# Projeto: Assistente de IA com Recuperação de Dados Aumentada (RAG) usando Embeddings, FAISS e PostgreSQL com Extensões Vetoriais

# Tecnologias utilizadas: 🖥⌨	
- Python
- OpenAI API para embeddings
- FAISS (Facebook AI Similarity Search)
- PostgreSQL com pgvector

# Sobre 📝	

 Objetivo do Projeto:

O objetivo do projeto é criar um assistente inteligente que combina técnicas de Recuperação de Dados Aumentada (RAG), usando embeddings para representar o conhecimento, com a capacidade de responder a perguntas complexas utilizando modelos de linguagem (como GPT) e uma base de conhecimento armazenada em um banco de dados vetorial. O sistema será capaz de gerar respostas precisas usando a combinação de embeddings e vetores de dados armazenados.
 Etapas do Projeto
 1. Geração de Embeddings
 Embeddings são representações vetoriais de textos, que mapeiam palavras ou frases para um espaço de alta dimensionalidade, capturando semântica e relações contextuais entre os termos. Usaremos uma biblioteca OpenAI para gerar embeddings a partir dos dados textuais.

 2. Armazenamento de Embeddings em Banco de Dados Vetorial
 Os embeddings gerados serão armazenados em um banco de dados vetorial que permite consultas eficientes por similaridade de vetores. Serão usadas duas abordagens principais:

 - FAISS (Facebook AI Similarity Search)
  O FAISS será utilizado para criar e pesquisar vetores em grandes bases de dados. FAISS é ideal para grandes volumes de dados devido à sua eficiência em buscas de similaridade.
 
 - PostgreSQL com Extensões Vetoriais (pgvector)
  Além do FAISS, usaremos o PostgreSQL com a extensão pgvector, que permite armazenar e consultar vetores de forma eficiente em um banco de dados relacional.

 3. Integração com Prompt e Modelo de Linguagem (RAG)
 O conceito de Recuperação de Dados Aumentada (RAG) combina a geração de respostas por modelos de linguagem com a recuperação de conhecimento de uma base externa (neste caso, os embeddings armazenados). A sequência básica será:

# Funcionamento 

 Entrada do Usuário: O usuário faz uma pergunta.
 Busca de Embedding Similar: Usar o embedding da pergunta para fazer uma busca de similaridade no banco de dados vetorial (usando FAISS ou PostgreSQL).
 Compor a Resposta: Recuperar os documentos mais relevantes do banco de dados, gerar uma resposta a partir deles usando um modelo de linguagem, e combinar essa resposta com o conteúdo gerado diretamente pelo modelo.

 Utilizando a Base de Conhecimento via Prompts
 Os dados recuperados através do processo RAG são utilizados para preencher o contexto de prompts enviados ao modelo de linguagem. O prompt é formatado de modo que o conteúdo relevante recuperado seja parte da entrada para o modelo

 # Conclusão do Projeto
Este projeto combina o poder dos modelos de linguagem com uma base de conhecimento vetorial eficiente. O uso de embeddings, juntamente com FAISS e PostgreSQL com pgvector, permite buscas rápidas e precisas por dados semânticos, e o modelo de linguagem (através de prompts) pode gerar respostas com base em conhecimento real armazenado.

# Imagens do projeto 📸	

<img width="346" alt="Screenshot 2024-10-17 121905" src="https://github.com/user-attachments/assets/74deec68-cebd-49c5-a597-ae2b60572488">
<img width="350" alt="Screenshot 2024-10-17 121919" src="https://github.com/user-attachments/assets/9518d2aa-b026-4252-9877-44b607e9797a">
