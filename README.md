# 🏛️ Sistema de Gerenciamento de Museu

![Language](https://img.shields.io/badge/Linguagem-C-blue)
![Data](https://img.shields.io/badge/Data-CSV-green)
![Tools](https://img.shields.io/badge/Tools-Excel%20Dashboard-success)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

## 📖 Sobre o Projeto

Este projeto é uma aplicação console desenvolvida em **C** que simula o funcionamento de um **Museu da Música Brasileira**. O software oferece uma experiência interativa onde o usuário pode "comprar" um ingresso, registrar sua visita e participar de um tour guiado através de quizzes sobre grandes artistas como Heitor Villa-Lobos, Tom Jobim, Dilermando Reis, Caetano Veloso e Ernesto Nazareth.

Além da aplicação principal, o projeto conta com um **Dashboard em Excel** integrado, que lê os dados gerados pelo sistema (em CSV) para apresentar estatísticas de visitação.

---

## 🚀 Funcionalidades

### 🖥️ Aplicação Console (C)
* **Bilheteria:** Sistema de cadastro de visitantes e emissão de ingressos.
* **Tour Interativo (Quiz):** O sistema lê perguntas e respostas de arquivos `.csv` organizados por artista e música.
* **Validação de Respostas:** Mecanismo de pontuação baseada no conhecimento do usuário.
* **Persistência de Dados:** Registro automático dos visitantes e logs no arquivo `BancoDeDados.csv`.

### 📊 Dashboard Analítico (Excel)
* **Visualização de Dados:** O arquivo `Dashboard.xlsm` consome o banco de dados CSV gerado pelo programa em C para criar gráficos e relatórios sobre o fluxo de visitantes.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** C (Lógica principal, manipulação de arquivos `FILE`, Ponteiros e Structs).
* **Banco de Dados:** Arquivos de texto plano (CSV).
* **Análise de Dados:** Microsoft Excel (Macros/VBA) para o Dashboard.

---

## ⚙️ Como Executar

Para rodar o projeto corretamente, é essencial manter a estrutura de pastas, pois o programa em C busca os arquivos de perguntas nos diretórios relativos.

### Pré-requisitos
* Um compilador C (GCC, MinGW ou IDEs como DevC++, Code::Blocks, VS Code).
* Microsoft Excel (para visualizar o Dashboard).

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/sistema-de-gerenciamento-de-museu.git](https://github.com/seu-usuario/sistema-de-gerenciamento-de-museu.git)
    ```

2.  **Compilar e Rodar:**
    * Navegue até a pasta raiz do projeto.
    * Compile o arquivo `Museu.c`.
    * **Importante:** Execute o programa a partir da pasta raiz para que ele consiga encontrar a pasta `Artistas/` e o arquivo `BancoDeDados.csv`.

3.  **Usar o Sistema:**
    * Siga as instruções no terminal para comprar o ingresso e escolher o artista.

4.  **Verificar Dashboard:**
    * Após utilizar o sistema, abra o `Dashboard.xlsm` e atualize os dados para ver as novas entradas refletidas nos gráficos.

---

## 📂 Estrutura de Arquivos

* `Museu.c`: Código fonte principal da aplicação.
* `BancoDeDados.csv`: Arquivo central onde os visitantes são registrados.
* `Dashboard.xlsm`: Planilha inteligente para análise gráfica.
* `Artistas/`: Contém subpastas (ex: `Tom Jobim`, `Caetano Veloso`) com os arquivos `.csv` de perguntas e respostas específicas de cada obra.
* `Programas Solos/`: Módulos isolados (como `bilheteria.c`) usados para testes unitários durante o desenvolvimento.
