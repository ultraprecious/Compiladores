# Compiladores
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
    - 2) As regras que relacionarem um A --> B , os iniciadores de A é a união de {} U First(B).
    
