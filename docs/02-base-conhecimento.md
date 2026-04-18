# Base de Conhecimento do Agente

## Dados Utilizados

Os dados foram estruturados para representar uma situação realista de uma pessoa com renda variável e objetivo claro (reserva de emergência). As transações mostram tanto receitas quanto despesas, permitindo ao agente Lúcio ensinar sobre orçamento, identificação de gastos supérfluos e planejamento de aportes. O histórico de atendimento serve como exemplo de interações anteriores, e os produtos financeiros são descritos de forma puramente educativa.

## Adaptações nos Dados

Os dados são fictícios e foram simplificados para evitar complexidades desnecessárias. Não há informações bancárias reais ou sensíveis. O foco é garantir consistência para que o agente possa gerar exemplos didáticos sem se perder em detalhes irrelevantes.

## Estratégia de Integração

A integração é feita via Python, utilizando `json.load()` para os arquivos JSON e `pandas.read_csv()` para os CSVs. Os dados são formatados como texto e concatenados ao prompt do sistema, seguindo a arquitetura definida na documentação do agente.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

**Dados do Cliente:**

- Nome: Mariana Costa
- Idade: 29 anos
- Perfil: Moderado
- Objetivo: Criar reserva de emergência para 6 meses
- Patrimônio total: R$ 12.000,00
- Reserva de emergência atual: R$ 3.500,00

**Últimas transações:**

- 02/03: Projeto design (Receita) + R$ 1.500,00
- 05/03: Aluguel (Moradia) - R$ 1.200,00
- 08/03: Supermercado (Alimentação) - R$ 420,00
- 10/03: Ifood (Alimentação) - R$ 70,00
- 12/03: Transferência poupança (Investimento) - R$ 300,00
- 15/03: Consultoria (Receita) + R$ 2.000,00
- 18/03: Farmácia (Saúde) - R$ 45,00
- 20/03: Uber (Transporte) - R$ 60,00
- 22/03: Conta de luz (Moradia) - R$ 130,00
- 25/03: Ifood (Alimentação) - R$ 55,00
- 28/03: Projeto design (Receita) + R$ 1.500,00
- 30/03: Reserva emergência (Investimento) - R$ 400,00

**Atendimentos anteriores:**

- 12/02: "Quanto devo guardar por mês para reserva?" → Resposta: guardar de 10% a 20% da renda.
- 18/02: "Onde devo deixar minha reserva de emergência?" → Resposta: poupança ou CDB com liquidez diária.
- 25/02: "E se eu precisar da reserva antes?" → Resposta: reserva é para ser usada em emergências.
