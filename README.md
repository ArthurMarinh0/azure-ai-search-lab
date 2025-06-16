# azure-ai-search-lab
Aplicação prática de Azure Cognitive Search com skillsets de IA para indexação e consulta inteligente de documentos.

# Azure Cognitive Search — Indexação e Consulta com AI Search

## 🔹 Etapas Realizadas

### 1. Ingestão de Conteúdo

- Criação de um container no **Azure Blob Storage** para armazenar documentos em formatos diversos (.pdf, .docx).
- Upload manual de arquivos representando conteúdo não estruturado (ex: contratos, relatórios, textos informativos).
- Configuração de uma **Data Source** no Azure Cognitive Search apontando para o container do Blob.

**Observação:** foi necessário garantir que os documentos estivessem legíveis e bem formatados para melhorar os resultados de OCR e análise semântica.

---

### 2. Criação de Skillset (Conjunto de Habilidades)

- Definição de um skillset personalizado com as seguintes habilidades cognitivas:
  - OCR (leitura de texto em imagens e PDFs)
  - Extração de entidades nomeadas (pessoas, organizações, locais)
  - Análise de sentimentos e linguagem natural
  - Key phrases (extração de termos relevantes)

- As habilidades foram conectadas ao pipeline de indexação usando os campos mapeados no schema do índice.

---

### 3. Configuração e Criação do Índice

- Definição do schema de índice com campos enriquecidos vindos do skillset (ex: `people`, `organizations`, `keyPhrases`, `content`).
- Habilitação de pesquisa semântica e filtros por categoria, data e entidades reconhecidas.
- Execução do **indexador** para processar todo o conteúdo e alimentar o índice.

**Resultado:** documentos passaram a estar pesquisáveis por palavras-chave, entidades, e até mesmo conceitos extraídos pela IA.

---

### 4. Consultas e Testes Práticos

- Realização de buscas simples e avançadas utilizando a API de pesquisa do Azure.
- Testes com consultas em linguagem natural e termos específicos como:
  - “Contratos assinados em 2022”
  - “Documentos mencionando a empresa X”
  - “Relatórios com sentimento negativo”
- Análise dos resultados com base na precisão, relevância e retorno semântico.

---

## 📌 Insights Obtidos

- Documentos de alta qualidade visual aumentam a taxa de sucesso na extração por OCR.
- O uso de **skillsets personalizados** permite enriquecer significativamente os dados e gerar índices mais inteligentes.
- A **busca semântica** oferece resultados mais contextuais e próximos da intenção do usuário, mesmo com termos ambíguos.
- É possível transformar arquivos brutos em **bases de conhecimento consultáveis** com mínimo esforço de codificação.
- A integração com o **Azure AI Services** abre possibilidades para análises mais profundas, como classificação, sumarização ou tradução automática no pipeline.



