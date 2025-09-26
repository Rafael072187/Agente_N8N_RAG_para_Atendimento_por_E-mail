📧 Agente RAG para Atendimento por E-mail

Este projeto implementa um agente de atendimento automatizado via e-mail, construído no n8n, que combina IA conversacional com uma arquitetura de RAG (Retrieval-Augmented Generation). Ele lê documentos do Google Drive, indexa em um vetor semântico no Pinecone, e utiliza essa base de conhecimento para responder automaticamente mensagens recebidas no Gmail.

---

🚀 Funcionalidades

📂 Monitoramento do Google Drive → novos arquivos adicionados são processados.

📑 Carregamento e divisão de documentos em blocos de texto otimizados.

🧠 Geração de embeddings (OpenAI) → indexação dos conteúdos no Pinecone.

✉️ Monitoramento de e-mails no Gmail → capta mensagens recebidas.

🤖 Agente de IA (GPT-4.1-mini) → interpreta os e-mails e busca contexto no Pinecone.

🧩 RAG (Retrieval-Augmented Generation) → respostas baseadas em dados atualizados.

💬 Resposta automática enviada no mesmo thread do Gmail.

🔄 Memória de curto prazo (últimas 10 interações) para manter o contexto da conversa.

---

🛠️ Tecnologias Utilizadas

Tecnologia	Finalidade

n8n	Orquestração do fluxo

Google Drive API	Entrada de novos documentos

Pinecone	Vetorização e busca semântica

OpenAI (Embeddings + GPT-4.1-mini)	IA para contexto e geração de respostas

LangChain Memory	Manutenção de contexto conversacional

Gmail API	Recebimento e envio de e-mails

---

📂 Estrutura do Fluxo

Google Drive Trigger → Monitora novos arquivos.

Download File + Data Loader → Carrega os documentos.

Recursive Text Splitter → Divide o conteúdo em partes menores.

Embeddings (OpenAI) → Converte textos em vetores.

Pinecone Vector Store → Indexa embeddings para busca futura.

Gmail Trigger → Detecta e-mails recebidos.

AI Agent → Consulta Pinecone, aplica memória e gera resposta.

Reply to Message (Gmail) → Envia a resposta automática ao remetente.

---

🎯 Casos de Uso

Atendimento ao cliente baseado em documentos internos.

Resposta automática de SAC com base em manuais, políticas e FAQs.

Assistente corporativo que responde e-mails com informações oficiais e atualizadas.

Redução de tempo gasto em respostas repetitivas, com ganho de consistência.
