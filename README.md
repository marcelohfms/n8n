# **Automação de Geração de Relatórios e Gráficos com GitHub Actions**

Este projeto tem como objetivo automatizar a execução de notebooks Jupyter, gerando gráficos e salvando os resultados diretamente em um repositório GitHub utilizando GitHub Actions.

---

## **Descrição**

O workflow automatiza as seguintes etapas:
1. Executa um notebook Jupyter chamado `Graficos_Relatorio_Performance.ipynb`.
2. Gera gráficos que são salvos na pasta `graficos_relatorio/`.
3. Atualiza automaticamente o repositório GitHub com os gráficos gerados.

---

## **Arquivos Principais**
- **`Graficos_Relatorio_Performance.ipynb`**: Notebook Jupyter responsável por processar os dados e gerar gráficos.
- **`graficos_relatorio/`**: Pasta onde os gráficos gerados são armazenados.
- **`.github/workflows/execute-notebook.yml`**: Arquivo de configuração do GitHub Actions que automatiza a execução do notebook.

---

## **Como Funciona**

1. **Trigger do Workflow**: O workflow é acionado via HTTP Request pelo N8N ou manualmente pelo GitHub Actions na aba **Actions** do repositório.
2. **Execução do Notebook**: 
   - O notebook é executado em um ambiente Python configurado automaticamente.
   - Bibliotecas como `pandas`, `numpy`, `matplotlib` e `openpyxl` são instaladas.
3. **Geração de Gráficos**: Os gráficos são gerados pelo notebook e salvos na pasta `graficos_relatorio/`.
4. **Atualização do Repositório**: 
   - Os gráficos gerados são automaticamente adicionados e enviados para o repositório GitHub.

---

## **Pré-requisitos**

Antes de utilizar este projeto, certifique-se de que:
- Você possui um token de acesso pessoal (PAT) configurado no repositório como um segredo chamado `GH_PAT`.
- O arquivo `Graficos_Relatorio_Performance.ipynb` está corretamente configurado para gerar os gráficos esperados.

---

## **Como Executar**

1. Faça um fork ou clone deste repositório.
2. Acesse a aba **Actions** no GitHub.
3. Escolha o workflow `Execute Notebook` e clique em **Run workflow**.
4. Após a execução, os gráficos serão atualizados automaticamente na pasta `graficos_relatorio/`.

---

## **Tecnologias Utilizadas**
- **Jupyter Notebook**
- **GitHub Actions**
- **Python**:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `openpyxl`

---

## **Contribuições**

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com melhorias e novas funcionalidades.

---

## **Licença**

Este projeto está licenciado sob a [Licença MIT](LICENSE).
