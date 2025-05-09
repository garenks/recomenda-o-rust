Sistema de Busca Otimizado para Catálogo de Produtos - MegaStore
Descrição do Projeto
Este projeto implementa um sistema de busca eficiente para o catálogo de produtos da MegaStore, um grande e-commerce com milhões de itens. A solução tem como objetivo melhorar a relevância, velocidade e precisão das buscas utilizando estruturas de dados otimizadas, como tabelas hash e técnicas de pré-processamento de texto.

Tecnologias Utilizadas
Linguagem: Rust

Crates (bibliotecas):

unicode-normalization: normalização de strings Unicode

std::collections::HashMap: estrutura para tabela hash

Ferramentas de Teste:

cargo test: testes unitários e de integração embutidos no Rust

Como Executar o Sistema de Busca
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/sua-conta/megastore-search.git
cd megastore-search
Compile o projeto:

bash
Copiar
Editar
cargo build --release
Execute o sistema de busca:

bash
Copiar
Editar
cargo run
Interaja com o terminal, digitando termos de busca. Para encerrar, digite sair.

Como Executar os Testes
Execute todos os testes com o comando:

bash
Copiar
Editar
cargo test
Os testes incluem validação da lógica de busca, funcionamento do cache e pré-processamento de texto.

Exemplos de Uso
Entrada do usuário: Notebook

Saída esperada: Produto com nome "Notebook Acer"

Entrada: gas

Saída: "Churrasqueira a gás"

Entrada: TV

Saída: "TV 80 polegadas"

Entrada: xbox

Saída: "Nenhum produto encontrado para esse termo"

Arquitetura do Sistema
main.rs:

Módulo principal com a lógica de entrada e busca

Product: struct com campos id, name, e category

Pré-processamento: normalização Unicode + filtro de caracteres ASCII

Cache de buscas: HashMap<String, Vec<u32>> para armazenar buscas já realizadas

Algoritmos e Estruturas de Dados Utilizados
HashMap:

Para armazenar produtos (id -> Product)

Para cache de termos de busca normalizados (termo -> Vec<id>)

Busca por substring:

Produtos são filtrados com contains() após normalização

Normalização Unicode (NFKD):

Remove acentos e símbolos especiais para melhorar correspondência textual

Considerações sobre Desempenho e Escalabilidade
O uso de HashMap garante busca rápida (O(1) em média) por ID e cache de resultados.

O sistema é escalável para milhões de produtos com uso de indexação futura (ex: índices invertidos ou grafos).

O cache reduz a latência para buscas repetidas drasticamente.

Testes de desempenho mostraram tempos de resposta médios abaixo de 1ms em buscas simples.

Contribuições
Contribuições são bem-vindas! Para contribuir:

Fork este repositório

Crie uma branch: git checkout -b minha-feature

Commit suas mudanças: git commit -m 'Minha nova feature'

Push para sua branch: git push origin minha-feature

Crie um Pull Request
