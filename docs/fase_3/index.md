# Fase 3 — Plano de Avaliação (Passo-a-passo)

## 1. Introdução

Este documento descreve o plano detalhado de execução da avaliação do sistema Cal.com, seguindo a metodologia GQM (Goal-Question-Metric) estabelecida na Fase 2. O foco está na implementação prática das métricas de **Adequação Funcional** e **Portabilidade** conforme o modelo de qualidade ISO/IEC 25010.

## 2. Objetivos da Fase 3

- **Operacionalizar** as métricas definidas na Fase 2 em procedimentos executáveis
- **Estabelecer** critérios claros para coleta e análise de evidências
- **Garantir** a rastreabilidade entre objetivos, questões e métricas
- **Fornecer** um guia completo para a execução consistente da avaliação

---

## 3. Visão Geral

Este documento descreve *como* executar a avaliação (passo a passo) para obter as medidas definidas na Fase 2 (métricas de Adequação Funcional e Portabilidade), como registrar evidências, calcular métricas e aplicar os critérios de julgamento. O plano está organizado por métrica: para cada uma há objetivos, passos de execução, entrada/saída, evidências exigidas e como calcular/julgar o resultado.

---

## 4. Metodologia de Avaliação

A avaliação seguirá uma abordagem sistemática baseada em:
- **Testes funcionais** para métricas de adequação funcional
- **Testes de instalação e configuração** para métricas de portabilidade
- **Avaliação subjetiva** por múltiplos avaliadores
- **Coleta sistemática** de evidências objetivas

### 4.1. Princípios de Avaliação
- **Reprodutibilidade**: Todos os testes devem ser replicáveis
- **Objetividade**: Evidências devem ser mensuráveis e verificáveis
- **Transparência**: Processos e critérios claramente documentados
- **Consistência**: Aplicação uniforme dos critérios de julgamento

---

### 4.2. Método de Avaliação (Resumo Estruturado)

| Etapa | Descrição | Responsável | Evidência |
|-------|-----------|-------------|-----------|
| **Preparação** | Configurar ambientes, templates e credenciais | Equipe | Checklist preenchido |
| **Execução** | Executar os testes definidos para cada métrica | Avaliadores | Prints, logs, formulários |
| **Registro** | Documentar resultados em planilha padronizada | Avaliadores | Planilha centralizada |
| **Cálculo** | Aplicar fórmulas para cada métrica | Responsável técnico | Planilha automatizada |
| **Julgamento** | Comparar resultados com critérios estabelecidos | Equipe | Relatório parcial |
| **Consolidação** | Criar relatório final com análise e recomendações | Grupo responsável | Documento final + anexos |

---

### 4.3 Instruções Gerais Para o Avaliador

Antes de iniciar:

1. Verificar se o ambiente está configurado conforme descrito na Seção 5.
2. Fazer login utilizando as credenciais fornecidas.
3. Garantir que **todos os templates estão disponíveis** (planilha, formulários, checklists).
4. Não modificar o fluxo dos testes ou interpretação das métricas.
5. **Registrar tudo**, mesmo erros inesperados ou dúvidas.

Durante a execução:

- Capturar evidências sempre que solicitado.
- Evitar **interpretações subjetivas** onde existe mensuração objetiva.
- Caso encontre erro, **registrar o passo exato e se o erro é reproduzível**.

Após a execução:

- Garantir que **toda evidência está armazenada corretamente**.
- Confirmar que os cálculos automáticos foram gerados corretamente.

---

## 5. Preparação (Artefatos e Templates Necessários)

### 5.1. Documentação de Suporte
- **Planilha padrão de coleta** com abas: `meta`, `execuções`, `logs`, `evidências` (colunas mínimas: métrica, id_teste, data, ambiente, passo, resultado, observação, link_evidência)
- **Template de caso de teste** para fluxos (passos numerados, entradas, saída esperada)
- **Checklist de evidências** (print screens, logs de API, timestamps, capturas de console)
- **Formulário de avaliação subjetiva** (escala 1-5 com critérios específicos)

### 5.2. Ambiente de Teste
- **Sistemas operacionais**: Ubuntu 22.04, Windows 11, macOS Sonoma
- **Navegadores**: Chrome (última versão), Firefox (última versão), Safari (última versão)
- **Dispositivos**: Desktop (resolução mínima 1920x1080), Notebook (1366x768)
- **Conexão**: Internet banda larga estável (mínimo 10 Mbps)

### 5.3 Infraestrutura de Armazenamento Planejado

| Item | Local | Obrigatório |
|-------|-------|-------------|
| Armazenamento de evidências | Google Drive | ✔ |
| Versionamento da planilha | GitHub do projeto | ✔ |
| Backup dos registros | Automático diário | ✔ |

---

## 6. Procedimento Geral de Execução (Válido para Todas as Métricas)

1. **Preparação**: Ler a definição da métrica e o critério de julgamento (Fase 2)
2. **Planejamento**: Preparar o(s) caso(s) de teste correspondente(s)
3. **Execução**: Executar o(s) teste(s) seguindo passos numerados
4. **Registro**: Registrar, linha a linha, os resultados na planilha padrão, incluindo *evidência* (print/log)
5. **Classificação**: Marcar cada execução como: `Sucesso`, `Parcial`, `Falha`
6. **Cálculo**: Ao final do conjunto de execuções da métrica, calcular a fórmula definida na Fase 2 e comparar com o critério de julgamento
7. **Conclusão**: Registrar conclusão comentada (se **Atende / Parcial / Não atende**) e adicionar observações (causa provável, reproducibilidade, impacto)

---

## 7. Plano por Métrica — Adequação Funcional

### 7.1. M1 — Cobertura Funcional Esperada

**Objetivo:** Verificar presença/acessibilidade das funções essenciais (agendar, reagendar, cancelar, integrar, notificar)

**Passos de Execução:**
1. Listar as funções essenciais esperadas (usar lista da Fase 2)
2. Navegar/inspecionar a aplicação e confirmar presença e acesso a cada função
3. Para cada função encontrada: capturar screenshot da UI e anotar o caminho/menu usado
4. Registrar ausências com descrição detalhada do que foi esperado vs. encontrado

**Entrada:** Lista de funções esperadas  
**Saída:** Número de funções implementadas  
**Evidência:** Screenshots + descrição do caminho + logs de navegação  
**Cálculo:** (implementadas ÷ esperadas) × 100  
**Critério de Julgamento:** 
- Excelente: ≥90%
- Boa: 75-89%
- Regular: 50-74%
- Insatisfatória: <50%

---

### 7.2. M2 — Taxa de Sucesso em Execução de Funcionalidades Principais

**Objetivo:** Medir confiabilidade das operações essenciais

**Passos de Execução:**
1. Definir 1 caso de teste por funcionalidade principal
2. Executar cada caso **3 vezes** (por definição da métrica)
3. Registrar resultado `Sucesso/Parcial/Falha` e capturar evidências (screenshot ou log)
4. Documentar falhas com stack trace quando disponível

**Entrada:** Casos de teste padronizados  
**Saída:** Nº de execuções bem-sucedidas / total  
**Cálculo:** (execuções bem-sucedidas ÷ total de execuções) × 100  
**Evidência:** Prints e logs por execução + timestamps  
**Critério de Julgamento:**
- Excelente: ≥95%
- Boa: 85-94%
- Regular: 70-84%
- Insatisfatória: <70%

---

### 7.3. M3 — Taxa de Sucesso dos Fluxos de Agendamento (5 Testes Completos)

**Objetivo:** Verificar fluxos ponta-a-ponta: criar, editar, reagendar, cancelar, excluir

**Passos de Execução:**
1. Montar 5 casos de fluxo (cada fluxo deve cobrir os passos listados)
2. Executar cada fluxo uma vez por execução planejada
3. Registrar resultado do fluxo inteiro (`Sucesso` somente se todas as etapas funcionarem)
4. Documentar desvios do fluxo esperado

**Entrada:** 5 casos de fluxo completos  
**Saída:** Nº de fluxos inteiros bem-sucedidos ÷ total testados  
**Evidência:** Sequência de screenshots por etapa + logs de sincronização (se aplicável)  
**Cálculo e Julgamento:** Conforme fórmula e faixas definidas

---

### 7.4. M4 — Ocorrência de Erros Visíveis Durante o Agendamento

**Objetivo:** Contar mensagens de erro/falhas visíveis durante os testes funcionais

**Passos de Execução:**
1. Durante as execuções de M2/M3, anotar toda mensagem de erro visível (texto, código, passo onde ocorreu)
2. Capturar screenshot do erro e coletar log relacionado (se houver)
3. Classificar erros por gravidade (bloqueante, não-bloqueante, cosmético)

**Entrada:** Execuções de testes  
**Saída:** Contador de erros por avaliador e por fluxo  
**Evidência:** Screenshots + logs + classificação de gravidade  
**Critério de Julgamento:**
- Excelente: 0 erros
- Boa: 1-2 erros não-bloqueantes
- Regular: 3-5 erros ou 1 erro bloqueante
- Insatisfatória: >5 erros ou múltiplos erros bloqueantes

---

### 7.5. M5 — Percentual de Funcionalidades Esperadas Ausentes

**Objetivo:** Identificar lacunas em relação a um produto de referência

**Passos de Execução:**
1. Definir lista de funcionalidades de referência (ex.: Calendly — usar lista curta e justificável)
2. Para cada item, checar se existe funcionalidade no Cal.com; anotar `Presente/Ausente/Parcial`
3. Justificar classificação "Parcial" com descrição das limitações

**Entrada:** Lista de referência (Calendly features)  
**Saída:** % ausentes  
**Evidência:** Evidência para cada item (UI/feature flag/documentação) + justificativa  
**Cálculo e Julgamento:** Aplicar fórmula e critérios

---

### 7.6. M6 — Número de Funcionalidades Redundantes Identificadas

**Objetivo:** Detectar duplicações funcionais

**Passos de Execução:**
1. Explorar menus e fluxos procurando ações com o mesmo propósito
2. Para cada duplicidade: documentar ambos os pontos com screenshots e explicar por que se trata de redundância
3. Avaliar impacto da redundância (confusão do usuário, manutenção extra)

**Entrada:** Exploração funcional sistemática  
**Saída:** Contador de redundâncias  
**Evidência:** Screenshots lado a lado + descrição + avaliação de impacto  
**Critério de Julgamento:**
- Excelente: 0 redundâncias
- Boa: 1-2 redundâncias de baixo impacto
- Regular: 3-4 redundâncias ou 1 de alto impacto
- Insatisfatória: >4 redundâncias ou múltiplas de alto impacto

---

### 7.7. M7 — Avaliação de Impacto Percebido pelos Avaliadores

**Objetivo:** Medir o impacto subjetivo de ausências/redundâncias

**Passos de Execução:**
1. Para cada ausência/redundância encontrada, atribuir nota 1–5 (1 = sem impacto, 5 = muito impacto)
2. Calcular média das notas
3. Coletar comentários qualitativos sobre o impacto

**Entrada:** Lista de problemas identificados (M5 e M6)  
**Saída:** Nota média de impacto  
**Evidência:** Formulário de avaliação preenchido por avaliador + comentários  
**Critério de Julgamento:**
- Excelente: ≤2.0
- Boa: 2.1-3.0
- Regular: 3.1-4.0
- Insatisfatória: >4.0

---

## 8. Plano por Métrica — Portabilidade

### 8.1. M1 — Taxa de Sucesso de Instalação em Múltiplos Ambientes

**Objetivo:** Validar se o software pode ser instalado corretamente em múltiplos ambientes

**Passos de Execução:**
1. Seguir instruções oficiais de instalação em pelo menos 3 ambientes distintos (Ubuntu, Windows, macOS)
2. Registrar para cada tentativa: sucesso/erro, ponto de falha e logs
3. Documentar workarounds necessários

**Entrada:** Documentação oficial e ambiente de instalação  
**Saída:** % instalações bem-sucedidas  
**Evidência:** Logs de instalação + screenshot do sistema em funcionamento + tempo de instalação  
**Cálculo/Julgamento:** Conforme faixas da Fase 2

---

### 8.2. M2 — Tempo Médio Estimado de Implantação

**Objetivo:** Medir o tempo até o sistema entrar em funcionamento

**Passos de Execução:**
1. Para cada instalação (M1), medir tempo total (início → aplicação acessível)
2. Registrar tempos e calcular média
3. Documentar etapas que consumiram mais tempo

**Entrada:** Medições de tempo reais  
**Saída:** Tempo médio em minutos  
**Evidência:** Timestamps + logs + breakdown por etapa  
**Critério de Julgamento:**
- Excelente: ≤30 min
- Boa: 31–60 min
- Regular: 61–120 min
- Insatisfatória: >120 min

---

### 8.3. M3 — Qualidade Percebida da Documentação de Instalação

**Objetivo:** Avaliar clareza/completude (nota 1–5)

**Passos de Execução:**
1. Após tentar instalar, cada avaliador atribui nota e comentários sobre lacunas
2. Avaliar especificamente: completude, clareza, exemplos, troubleshooting

**Entrada:** Experiência de instalação  
**Saída:** Média de notas e comentários qualitativos  
**Evidência:** Formulário preenchido + notas específicas por seção  
**Critério de Julgamento:**
- Excelente: ≥4.5
- Boa: 3.5-4.4
- Regular: 2.5-3.4
- Insatisfatória: <2.5

---

### 8.4. M4 — Esforço de Implantação Percebido

**Objetivo:** Medir esforço cognitivo/técnico (1–5)

**Passos de Execução:**
1. Cada avaliador classifica o esforço (1 = muito fácil, 5 = muito difícil) e descreve passos críticos que demandaram esforço
2. Identificar pontos de maior complexidade

**Entrada:** Experiência de instalação  
**Saída:** Média de notas e comentários qualitativos  
**Evidência:** Formulário preenchido + descrição de desafios  
**Critério de Julgamento:**
- Excelente: ≤2.0
- Boa: 2.1-3.0
- Regular: 3.1-4.0
- Insatisfatória: >4.0

---

### 8.5. M5 — Compatibilidade Entre Navegadores

**Objetivo:** Verificar que fluxos principais funcionam sem erro nos navegadores-alvo

**Passos de Execução:**
1. Executar os mesmos fluxos principais (criar, reagendar, cancelar) em cada navegador
2. Registrar `Sucesso/Parcial/Falha` e evidências
3. Testar funcionalidades JavaScript intensivas

**Entrada:** Casos de teste padronizados  
**Saída:** % fluxos sem erro por navegador  
**Evidência:** Screenshots por navegador e logs JS/network (se aplicável)  
**Critério de Julgamento:**
- Excelente: 100% em todos navegadores
- Boa: ≥90% em todos navegadores
- Regular: ≥80% em maioria dos navegadores
- Insatisfatória: <80% em qualquer navegador

---

### 8.6. M6 — Compatibilidade Entre Dispositivos

**Objetivo:** Verificar funcionalidade/legibilidade em desktop/mobile (ou emulador)

**Passos de Execução:**
1. Executar fluxos principais em cada categoria de dispositivo
2. Registrar erros de funcionalidade ou degradação de interface
3. Avaliar responsividade e usabilidade em mobile

**Entrada:** Casos de teste responsivos  
**Saída:** % funcionalidade mantida por dispositivo  
**Evidência:** Screenshots em cada dimensão de tela + métricas de usabilidade  
**Cálculo/Julgamento:** Conforme Fase 2

---

### 8.7. M7 — Clareza e Autonomia na Configuração das Dependências Externas

**Objetivo:** Avaliar se dependências (DB, e-mail, APIs) podem ser configuradas seguindo a documentação sem necessidade de suporte ou ajuda de terceiros

**Passos de Execução:**
1. Tentar configurar ao menos um serviço externo (ex.: envio de e-mail) seguindo documentação
2. Registrar passos que exigiram pesquisa/ajuda externa
3. Avaliar completude das instruções

**Entrada:** Documentação de configuração  
**Saída:** Nota de autonomia (1-5)  
**Evidência:** Logs de configuração + notas sobre gaps na doc  
**Critério de Julgamento:**
- Excelente: Configuração totalmente autônoma
- Boa: Pequenas consultas necessárias
- Regular: Múltiplas consultas necessárias
- Insatisfatória: Impossível sem ajuda externa

---

## 9. Cronograma de Execução

| Fase | Atividade | Duração | Responsáveis |
|------|-----------|---------|-------------|
| Preparação | Configuração de ambientes e templates | 2 dias | Equipe completa |
| Execução M1-M7 (Funcional) | Testes de adequação funcional | 5 dias | Gustavo, Atyrson, Vinicius |
| Execução M1-M7 (Portabilidade) | Testes de instalação e compatibilidade | 4 dias | Cairo, Antonio, Pedro |
| Consolidação | Análise e relatório final | 3 dias | Equipe completa |

---

## 10. Riscos e Mitigações

| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|
| Ambiente de teste inconsistente | Alta | Médio | Padronização prévia e checklist de verificação |
| Falha na reprodução de bugs | Média | Alto | Captura sistemática de evidências e steps-to-reproduce |
| Viés do avaliador | Média | Médio | Múltiplos avaliadores e critérios objetivos |
| Limitações de tempo | Alta | Médio | Priorização baseada em critérios de criticidade |

---

## 11. Consolidação, Análise e Julgamento (Após Execução de Todas as Métricas)

### 11.1. Processo de Consolidação
1. **Agregação**: Consolidar todas as linhas das planilhas em uma aba mestre
2. **Cálculo automático**: Usar fórmulas para cada métrica (pré-configuradas na planilha) para obter percentuais e médias
3. **Classificação final por métrica**: Aplicar faixas (Excelente/Boa/Regular/Insatisfatória) já definidas
4. **Síntese por característica**: Computar score agregado para *Adequação Funcional* e *Portabilidade* (média ponderada das métricas)

### 11.2. Análise de Resultados
5. **Registro de problemas críticos**: Listar testes que falharam com evidências e passos para reproduzir
6. **Identificação de padrões**: Agrupar falhas por tipo, gravidade e área funcional
7. **Análise de correlação**: Verificar relações entre métricas (ex.: M2 e M4)

### 11.3. Relatório Final
8. **Recomendações**: Para métricas abaixo do aceitável, indicar causa provável e ação corretiva sugerida
9. **Relatório final**: Incluir objetivo, método, tabelas de métricas, gráficos simples (percentual de conformidade) e anexos com evidências
10. **Apresentação executiva**: Sumário para stakeholders com foco em resultados e recomendações

---

## 12. Critérios de Aceitação Globais (Aplicáveis ao Relatório)

- **Rastreabilidade completa**: Todas as métricas possuem evidência anexada (screenshot ou log)
- **Consistência metodológica**: Todas as métricas foram calculadas e comparadas com critérios da Fase 2
- **Clareza nos resultados**: Cada métrica tem resultado classificado como `Atende / Parcial / Não atende`
- **Foco em ações**: O relatório indica claramente quais problemas são críticos e quais são de baixa prioridade
- **Transparência**: Limitações da avaliação são explicitamente declaradas
- **Reprodutibilidade**: Procedimentos suficientemente detalhados para replicação

## 13. Conclusão do Método de Avaliação

O método documentado garante que qualquer avaliador — independente de participação prévia — consiga conduzir o processo de forma **objetiva, repetível e rastreável**, atendendo aos requisitos da docente:

- Explica **como avaliar**
- Define **o que registrar**
- Determina **recursos necessários**
- Apresenta **cronograma**
- Oferece **método padronizado aplicável a qualquer ambiente**

---

## 14. Referências

> SILVA, Carlos Vinícius Pereira da; MOURA, Déborah Carvalho de; CAMPOS, Danylo de Castro; NERY, Paulo. *GQM: Goal - Question - Metric*. 2009.

> BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, H. Dieter. *Goal Question Metric Paradigm*. In: MARCINIAK, John J. (Ed.). Encyclopedia of Software Engineering - 2° Vol. New York: John Wiley & Sons, Inc., 1994.

> ISO/IEC 25010:2011. Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models.

---

## 15. Histórico de Versões

| Versão | Data       | Descrição                                                               | Autor                               |
| :----- | :--------- | :---------------------------------------------------------------------- | :---------------------------------- |
| `1.0`  | 16/11/2025 | Criação da estrutura inicial do plano de avaliação passo-a-passo | [Gustavo Haubert](https://github.com/GustavoHaubert) |
| `1.1`  | 16/11/2025 | Expansão com seções de introdução, objetivos, metodologia e cronograma | [Pedro Braga](https://github.com/Stain19) |
| `1.2`  | 16/11/2025 | Adição de riscos e mitigações, e refinamento dos critérios de julgamento | [Pedro Braga](https://github.com/Stain19) |
| `1.3`  | 16/11/2025 | Expansão detalhada de todas as métricas com procedimentos executáveis | [Pedro Braga](https://github.com/Stain19) |
| `1.4` | 16/11/2025 | Complementação com instruções ao avaliador, infraestrutura necessária e conclusão do método conforme exigências da professora | [Antonio Carvalho](https://github.com/antonioscarvalho) |