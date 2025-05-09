# Sistema de Busca Otimizado para Catálogo de Produtos - MegaStore

## 📘 Descrição do Projeto

Este projeto implementa um sistema de busca eficiente para o catálogo de produtos da MegaStore, um e-commerce com milhões de itens. O objetivo é oferecer resultados relevantes com alta performance, utilizando estruturas como **tabelas hash** e **normalização de texto**, além de um mecanismo de **cache** para buscas repetidas.

## 🛠 Tecnologias Utilizadas

- **Linguagem:** [Rust](https://www.rust-lang.org/)
- **Crates (bibliotecas):**
  - [`unicode-normalization`](https://docs.rs/unicode-normalization): para normalizar textos e remover acentuação
- **Ferramentas:**
  - `cargo`: gerenciador de pacotes e builds do Rust
  - `cargo test`: sistema de testes integrados

## 🚀 Como Executar o Sistema de Busca




🧪 Como Executar os Testes
bash
Copiar
Editar
# Executa todos os testes unitários e de integração
cargo test
💡 Exemplos de Uso
Entrada do Usuário	Resultado Esperado
Notebook	Produto com nome "Notebook Acer"
gas	"Churrasqueira a gás"
TV	"TV 80 polegadas"
xbox	Nenhum produto encontrado

🏗 Arquitetura do Sistema
main.rs: módulo principal

Product: estrutura com campos id, name e category

preprocess(): função de normalização e limpeza de texto

HashMap<u32, Product>: armazena os produtos por ID

HashMap<String, Vec<u32>>: cache de buscas para acelerar resultados repetidos

🧠 Algoritmos e Estruturas de Dados Utilizados
Tabelas Hash (HashMap):

Para armazenar produtos por ID

Para cachear termos de busca

Normalização Unicode (NFKD):

Remove acentuação e caracteres especiais

Torna as buscas mais robustas

Filtro por substring:

Produtos são filtrados com contains() sobre nomes normalizados

⚙️ Considerações sobre Desempenho e Escalabilidade
Busca em O(1) para produtos via ID e para cache de buscas

Normalização permite buscas mais inclusivas e sem erros por acento

Cache reduz o tempo de resposta para termos já consultados

Estrutura pronta para ser estendida com grafos e indexadores invertidos para suportar escala maior

🤝 Contribuições
Contribuições são bem-vindas! Para colaborar:

Faça um fork deste repositório

Crie uma branch com sua feature: git checkout -b minha-feature

Commit suas mudanças: git commit -m 'Adiciona nova feature'

Faça push da branch: git push origin minha-feature

Abra um Pull Request
