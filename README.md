#  Lúcio – Agente Educador Financeiro com IA Generativa

## Contexto

Os assistentes virtuais no setor financeiro estão evoluindo de simples chatbots reativos para **agentes inteligentes e proativos**. Neste desafio, foi desenvolvido o **Lúcio**, um agente educador financeiro que utiliza IA Generativa para:

- **Ensinar conceitos** de finanças pessoais de forma simples e personalizada
- **Usar dados do cliente** (mockados) para criar exemplos práticos
- **Garantir segurança** e evitar recomendações inadequadas (anti-alucinação)
- **Manter tom acolhedor** e nunca julgar as dúvidas do usuário

---

## Aplicação Funcional (Google Colab)

O agente **Lúcio** está disponível e funcionando diretamente no Google Colab, com interface interativa via **Gradio**. Basta executar o notebook e fornecer sua chave da OpenAI (a chave **não fica salva** no código).

🔗 **Acesse o notebook funcional no repositório:**  
`Agente_de_IA_financeiro_LÚCIO (1).ipynb`

ou diretamente no botão abaixo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pepineli/dio-lab-bia-do-futuro/blob/main/Agente_de_IA_financeiro_L%C3%9ACIO%20(1).ipynb)

> **Nota:** Ao executar, o notebook solicitará sua chave da OpenAI via `getpass`. A chave **não fica salva** no código, garantindo segurança. Você precisa ter créditos na OpenAI (mínimo US$ 5).

---

##  O Que Foi Entregue

### 1. Documentação do Agente

- **Caso de Uso:** Educação financeira para pessoas com renda variável (cliente mockada Mariana)
- **Persona e Tom de Voz:** Lúcio – paciente, acolhedor, informal
- **Arquitetura:** Google Colab + Gradio + API OpenAI (GPT-3.5-turbo)
- **Segurança:** Regras rígidas contra alucinação e proibição de recomendações

📄 `docs/01-documentacao-agente.md`

### 2. Base de Conhecimento

Dados mockados da cliente **Mariana Costa** (renda variável, objetivo: reserva de emergência).

| Arquivo | Formato | Descrição |
|---------|---------|-----------|
| `transacoes.csv` | CSV | Últimas 12 transações |
| `historico_atendimento.csv` | CSV | 3 interações anteriores |
| `perfil_investidor.json` | JSON | Perfil moderado, patrimônio R$ 12k |
| `produtos_financeiros.json` | JSON | Descrições educativas de produtos |

📄 `docs/02-base-conhecimento.md`

### 3. Prompts do Agente

System prompt com regras de segurança, exemplos de interação e tratamento de edge cases.

📄 `docs/03-prompts.md`

### 4. Código Funcional

- Notebook Colab com interface Gradio (arquivo principal)
- Código alternativo para Streamlit (pasta `src/` – não mantido ativamente)

📁 `Agente_de_IA_financeiro_LÚCIO (1).ipynb`  
📁 `src/` (código legado)

### 5. Avaliação e Métricas

Métricas de assertividade, segurança, coerência e plano de testes.

📄 `docs/04-metricas.md`

### 6. Pitch

Roteiro de 3 minutos para apresentação do agente.

📄 `docs/05-pitch.md`

---

## Status do Projeto

| Etapa | Status |
|-------|--------|
| Documentação (`docs/`) | ✅ Concluída |
| Base de conhecimento (`data/`) | ✅ Concluída |
| Código funcional (Colab + Gradio) | ✅ Concluído |
| README e estrutura do repositório | ✅ Concluído |
| Segurança (chave não exposta) | ✅ Garantida |

---

> ⚠️ O agente **não funciona localmente com Streamlit** devido a limitações de memória no computador. Portanto foi realizada no colab.
---

##  Segurança e Privacidade

- **Nenhuma chave de API** está exposta nos arquivos do repositório.
- O notebook Colab utiliza `getpass` para ler a chave em tempo real.
- Os dados são **mockados** (fictícios) – não há informações sensíveis reais.

---

##  Agradecimentos

- **DIO** pelo bootcamp e desafio
- **Bradesco** pela oportunidade
- **OpenAI** pela API do ChatGPT
- **Gradio** pela interface interativa

---

## 📄 Licença

Projeto educacional desenvolvido para o **Bootcamp Bradesco GenAI & Dados** da DIO.

---

**Desenvolvido por Murilo Pepineli**  
[GitHub](https://github.com/pepineli) | [LinkedIn](https://linkedin.com/in/pepineli)
