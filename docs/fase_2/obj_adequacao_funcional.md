## 1° Objetivo de Medição: Adequação Funcional

| Elemento | Descrição |
| :-- | :-- |
| Analisar | o software Cal.com |
| Com propósito de | avaliar sua qualidade funcional |
| A respeito de | Adequação Funcional |
| Do ponto de vista de | usuários do sistema |
| No contexto de | avaliação da qualidade de software segundo o modelo ISO/IEC 25010 |

**Tabela 1 – 1° Objetivo de Medição: Adequação Funcional**

#### Q1 – Funcionalidades Principais
As funcionalidades principais do sistema (agendamento, notificação e integração com Google Calendar e Outlook) estão implementadas conforme o esperado para um software de agendamento?

- **Hipót. H1.1:** O Cal.com implementa a maioria das funcionalidades essenciais, atendendo aos requisitos esperados para um sistema de agendamento.

---

#### Q2 – Correção de Operação
As funções centrais de agendamento (criação, edição, cancelamento e reagendamento) funcionam corretamente e de forma previsível?

- **Hipót. H2.1:** As funcionalidades principais operam corretamente na maioria dos cenários, com falhas menores não críticas.

---

#### Q3 – Completude Funcional
Existem funcionalidades redundantes ou ausentes?

- **Hipót. H3.1:** O sistema possui as funcionalidades adequadas para seu propósito, com eventuais ausências secundárias.

---

#### Q4 – Impacto das Funcionalidades Ausentes
Qual o nível de impacto de funcionalidades ausentes ou redundantes para o uso do sistema?

- **Hipót. H4.1:** A ausência de funções secundárias pode impactar usuários avançados, mas não compromete o fluxo principal.

---

#### Q5 – Consistência Entre Navegadores
Qual o nível de consistência do uso do software entre diferentes navegadores e sessões?

- **Hipót. H5.1:** O sistema mantém comportamento consistente, garantindo respostas previsíveis e uniformes na maioria dos cenários de uso.

---

### Métricas Relacionadas

| **Código** | **Métrica** | **Tipo** | **Descrição** | **Critério de Julgamento** |
|:--:|:--|:--|:--|:--|
| **M1** | Cobertura funcional esperada | Quantitativa | Verificar quantas funcionalidades essenciais (agendar, reagendar, cancelar, integrar, notificar) estão implementadas e acessíveis.<br>**Fórmula:** (Nº funcionalidades implementadas ÷ Nº esperadas) × 100 | ≥ 90% = Excelente <br>70–89% = Regular <br><70% = Insatisfatória |
| **M2** | Taxa de sucesso em execução de funcionalidades principais | Quantitativa | Executar cada funcionalidade principal ao menos 3 vezes e calcular.<br>**Fórmula:** (Execuções bem-sucedidas ÷ Total de execuções) × 100 | ≥ 95% = Excelente <br>85–94% = Boa <br><85% = Insatisfatória |
| **M3** | Taxa de sucesso dos fluxos de agendamento | Quantitativa | Realizar 5 testes completos (criar, editar, reagendar, cancelar).<br>**Fórmula:** (Fluxos bem-sucedidos ÷ Total de testes) × 100 | 100% = Excelente <br>90–99% = Regular <br><90% = Insatisfatória |
| **M4** | Ocorrência de erros visíveis durante o agendamento | Quantitativa | Contar mensagens de erro, falhas na interface ou inconsistências em cada teste funcional. | 0–2 = Excelente <br>3–5 = Regular <br>>5 = Insatisfatória |
| **M5** | Percentual de funcionalidades esperadas ausentes | Quantitativa | Identificar funcionalidades essenciais em outras aplicações de agendamento mas não encontradas na aplicação.<br>**Fórmula:** (Ausentes ÷ Esperadas) × 100 | ≤ 5% = Excelente <br>6–15% = Regular <br>>15% = Insatisfatória |
| **M6** | Número de funcionalidades redundantes identificadas | Quantitativa | Contar funções que duplicam propósitos (ex.: dois modos diferentes de cancelar o mesmo evento). | 0–1 = Excelente <br>2–3 = Regular <br>>3 = Insatisfatória |
| **M7** | Avaliação de impacto percebido pelos avaliadores | Qualitativa | Atribuir notas de 1 (sem impacto) a 5 (muito impacto) para cada função ausente ou redundante e calcular a média. | ≤ 2 = Excelente <br>3 = Regular <br>>3 = Insatisfatória |
| **M8** | Compatibilidade entre navegadores | Quantitativa | Executar fluxos idênticos (criar, cancelar, reagendar) em Chrome, Firefox e Safari.<br>**Fórmula:** (Fluxos sem erro ÷ Total de fluxos testados) × 100 | ≥ 95% = Excelente <br>80–94% = Boa <br><80% = Insatisfatória |
