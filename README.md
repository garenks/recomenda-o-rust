# Sistema de Busca Otimizado para Catálogo de Produtos - MegaStore

## Descrição do Projeto

Este projeto implementa um sistema de busca eficiente para o catálogo de produtos da MegaStore, um e-commerce com variações de itens. O objetivo é oferecer resultados relevantes com alta performance, utilizando estruturas como **tabelas hash** e **normalização de texto**, além de um mecanismo de **cache** para buscas repetidas.

## Tecnologias Utilizadas

- **Linguagem:** [Rust](https://www.rust-lang.org/)
- **Crates (bibliotecas):**
  - [`unicode-normalization`]: para normalizar textos e remover acentuação
- **Ferramentas:**
  - `cargo`: gerenciador de pacotes e builds do Rust
  - `cargo test`: sistema de testes integrados
 
### Testes realizados:
- Teste de normalização de texto (remoção de acentos e caracteres especiais).
- Teste de preservação de caracteres alfanuméricos e espaços na normalização.
- Teste de busca por nome de produto com correspondência parcial.
- Teste de funcionamento do cache de buscas.
- Teste de retorno vazio quando nenhum produto é encontrado.

# Como Executar o Sistema de Busca

### Compile o projeto
cargo build --release

## Execute o sistema
cargo run

### Instruções de como executar o sistema de busca

### Compile o projeto:
cargo build --release


### Execute o sistema de busca:
cargo run


## Instruções de como executar os testes
  O projeto utiliza testes unitários e testes de integração. Para executá-los:
cargo test


## Exemplos de uso
  Ao executar o sistema, você verá um prompt no terminal:
Digite um termo de busca (ou 'sair' para encerrar):


## Arquitetura do sistema:

* src/main.rs: Interface de linha de comando.

* Utiliza HashMap para estruturação e cache dos produtos.


## Algoritmos e estruturas de dados utilizados

* Tabela Hash (HashMap):

* Para armazenar o catálogo de produtos.

* Para cachear termos de busca normalizados e acelerar resultados subsequentes.

* Normalização Unicode (unicode-normalization):

* Utilizada para remover acentuação e tornar as buscas mais robustas.


## Considerações sobre desempenho e escalabilidade

* O uso de HashMap garante busca em tempo constante para acessos diretos por ID e para cache.

* O sistema utiliza normalização de strings para melhorar a relevância da busca.

* A cache de buscas reduz bastante o tempo de resposta para consultas repetidas.

* A modularização do código e separação entre binário e biblioteca permite fácil expansão e paralelização futura.
