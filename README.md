# Compiladores 

## Aula 2.1 : Revisão de linguagens
  - Gramáticas First e Follow (Gramáticas livres de contexto --> Um símbolo não terminal deriva qualquer sequência não terminal.

  - Uma gramática é uma quádrupla ordenada composta por:
    Simbolos terminais, símbolos não terminais, regras de produção, um não terminal especial S (inicial).

  - First : "Cabeça" de uma cadeia de símbolos. Dado uma regra, a cabeça é o primeiro elemento do lado direito dessa regra.
  - Último/Last/Tail : Dada uma regra, é o último elemento do lado direito dessa regra.

  - Geração de cadeia vazia:
    1) Eliminar regras que contém um símbolo terminal (letra minuscula)
    2) Eliminar as regras que levam um não terminal derivando um vazio. Escrever SIM para os não terminais que isso ocorrer.
    3) Apagar os não terminais que derivam vazio que se encontram à direita
    4) Digitar não para os que não conseguem derivar cadeia vazia. 

  ## INICIADORES
    - 1) Pega os primeiros elementos não terminais de cada regra
    - 2) As regras que relacionarem um A --> B , os iniciadores de A é a união de {} U First(B).<img width="517" height="331" alt="image" src="https://github.com/user-attachments/assets/b752161a-aa9b-4722-9110-4e48bce2d235" />

    

## Aula 2.2 - Análise sintática
  - Enquanto a analise léxica se preocupa com identificar lexemas e enquadrá-los em tokens, um analisador sintático se preocupa em analisar o conjunto de lexemas válidos e concluir se eles formam uma expressão válida e reconhecida pela gramática. Se preocupa com a sequência de símbolos válidos.
  - Utiliza estruturas de dados: recursivas e árvores
  - Derivação : é o processo de substituir símbolos não terminais por terminais, existindo duas classificações:
      - Derivação pela esquerda: Começa substituindo o não terminal mais a esquerda.
      - Derivação pela direita: Começa substituindo o não terminal mais a direita.
  - Por ser a segunda etapa, o analisador léxico realizou o trabalho de conferir se os caracteres são válidos. Agora, é a vez do analisador sintático analisar se as expressões formadas são válidas. Isso será realizado através de uma varredura. O melhor caminho para realizá-la é utilizando AFD's. Existem duas categorias de varredura:
      - Ascendente/bottom up: Inicia a partir das folhas em direção à raiz --> Parte dos símbolos terminais e tenta adivinhar o não terminal que gerou aquela cadeia.
        - <img width="517" height="331" alt="Derivação Topdown" src="https://github.com/user-attachments/assets/03846eec-d002-4074-ba6e-57c9e1a382f0" />


      - Descendente/Top Down :Inicia na raíz da árvore e segue para as folhas --> Parte dos símbolos inicial e tenta adivinhar qual das regras aplicar a partir dos símbolos lidos.
        - <img width="534" height="312" alt="image" src="https://github.com/user-attachments/assets/24920b2d-d5cc-40ff-8c76-606deb98c09f" />

    
