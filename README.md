# 🤖 Lúcio – Agente Educador Financeiro com IA Generativa

## Contexto

Os assistentes virtuais no setor financeiro estão evoluindo de simples chatbots reativos para **agentes inteligentes e proativos**. Neste desafio, desenvolvemos o **Lúcio**, um agente educador financeiro que utiliza IA Generativa para:

- **Ensinar conceitos** de finanças pessoais de forma simples e personalizada
- **Usar dados do cliente** (mockados) para criar exemplos práticos
- **Garantir segurança** e evitar recomendações inadequadas (anti-alucinação)
- **Manter tom acolhedor** e nunca julgar as dúvidas do usuário

---

## O Que Foi Entregue

### 1. Documentação do Agente

Definimos o **Lúcio**, um educador financeiro paciente e informal, que ensina sobre reserva de emergência, orçamento e produtos financeiros sem recomendar investimentos.

- **Caso de Uso:** Educação financeira para pessoas com renda variável (ex: Mariana, nossa cliente mockada)
- **Persona e Tom de Voz:** Acolhedor, informal, como um amigo mais experiente
- **Arquitetura:** Streamlit + Ollama (ou API Gemini) + base de conhecimento JSON/CSV
- **Segurança:** Regras rígidas contra alucinação e proibição de recomendações

📄 **Arquivo:** `docs/01-documentacao-agente.md`

---

### 2. Base de Conhecimento

Adaptamos os dados mockados para o perfil da **Mariana Costa** (29 anos, renda variável, objetivo: reserva de emergência). Os arquivos estão prontos para alimentar o agente:

| Arquivo | Formato | Descrição |
|---------|---------|-----------|
| `transacoes.csv` | CSV | Últimas 12 transações (receitas e despesas) |
| `historico_atendimento.csv` | CSV | 3 interações anteriores sobre reserva de emergência |
| `perfil_investidor.json` | JSON | Perfil moderado, patrimônio R$ 12k, reserva atual R$ 3,5k |
| `produtos_financeiros.json` | JSON | Descrições educativas de poupança, CDB, Tesouro Direto e fundos |

📄 **Documentação:** `docs/02-base-conhecimento.md`

---

### 3. Prompts do Agente

Documentamos o **system prompt** com regras rígidas de segurança, exemplos de interação (educacional, limitação, edge cases) e estratégias para evitar alucinações.

📄 **Arquivo:** `docs/03-prompts.md`

---

### 4. Aplicação Funcional (em desenvolvimento)

O código fonte do agente está sendo implementado na pasta `src/`.  
Tecnologias sugeridas: Streamlit, Ollama (local) ou API Gemini, e integração com os dados mockados.

📁 **Pasta:** `src/`

---

### 5. Avaliação e Métricas

Definimos métricas de **assertividade, segurança e coerência**, além de um plano de testes com cenários reais (consulta de gastos, recomendação proibida, perguntas fora do escopo).

📄 **Arquivo:** `docs/04-metricas.md`

---

### 6. Pitch

Roteiro de 3 minutos apresentando o problema (falta de personalização na educação financeira), a solução (Lúcio com dados mockados), a demonstração (três interações) e o diferencial (cuidado com o usuário e redução da ansiedade financeira).

📄 **Arquivo:** `docs/05-pitch.md`

---

## Status do Projeto

✅ **Documentação concluída** (todas as seções `docs/` preenchidas)  
✅ **Base de conhecimento definida** (arquivos `data/` adaptados)  
🔄 **Implementação do código** em andamento (pasta `src/` em breve)  
⏳ **Pitch** a ser gravado e anexado

---

## Ferramentas Utilizadas (previstas)

| Categoria | Ferramentas |
|-----------|-------------|
| **LLMs** | Ollama (local) ou API Gemini |
| **Desenvolvimento** | Streamlit, Python, Google Colab |
| **Dados** | JSON, CSV |
| **Diagramas** | Mermaid |

---

## Estrutura do Repositório
📁 dio-lab-bia-do-futuro/  
│  
├── 📄 README.md  
│  
├── 📁 data/ # Dados mockados (Mariana Costa)  
│ ├── historico_atendimento.csv  
│ ├── perfil_investidor.json  
│ ├── produtos_financeiros.json  
│ └── transacoes.csv  
│  
├── 📁 docs/ # Documentação completa  
│ ├── 01-documentacao-agente.md  
│ ├── 02-base-conhecimento.md  
│ ├── 03-prompts.md  
│ ├── 04-metricas.md  
│ └── 05-pitch.md  
│  
├── 📁 src/ # Código (em desenvolvimento)  
│ └── app.py  
│  
└── 📁 assets/ # Imagens e diagramas (opcional)  

---

## Como Executar (assim que o código estiver pronto)

1. Clone o repositório  
2. Instale as dependências: `pip install -r requirements.txt`  
3. Execute o agente: `streamlit run src/app.py`

---

## Licença

Projeto educacional desenvolvido para o **Bootcamp Bradesco GenAI & Dados** da DIO.

---

**Desenvolvido por Murilo Pepineli**  
[GitHub](https://github.com/pepineli) | [LinkedIn](https://linkedin.com/in/pepineli)
