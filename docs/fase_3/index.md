# Fase 3 — Plano de Avaliação (Passo-a-passo)

## Visão geral
Este documento descreve *como* executar a avaliação (passo a passo) para obter as medidas definidas na Fase 2 (métricas de Adequação Funcional e Portabilidade), como registrar evidências, calcular métricas e aplicar os critérios de julgamento. O plano está organizado por métrica: para cada uma há objetivos, passos de execução, entrada/saída, evidências exigidas e como calcular/julgar o resultado.

---

## Preparação (artefatos e templates necessários — preparar antes de executar)
- **Planilha padrão de coleta** com abas: `meta`, `execuções`, `logs`, `evidências` (colunas mínimas: métrica, id_teste, data, ambiente, passo, resultado, observação, link_evidência).
- **Template de caso de teste** para fluxos (passos numerados, entradas, saída esperada).
- **Checklist de evidências** (print screens, logs de API, timestamps, capturas de console).

---

## Procedimento geral de execução (válido para todas as métricas)
1. Ler a definição da métrica e o critério de julgamento (Fase 2).  
2. Preparar o caso(s) de teste correspondente(s). 
3. Executar o(s) teste(s) seguindo passos numerados.  
4. Registrar, linha a linha, os resultados na planilha padrão, incluindo *evidência* (print/log).  
5. Marcar cada execução como: `Sucesso`, `Parcial`, `Falha`.  
6. Ao final do conjunto de execuções da métrica, calcular a fórmula definida na Fase 2 e comparar com o critério de julgamento.  
7. Registrar conclusão comentada (se **Atende / Parcial / Não atende**) e adicionar observações (causa provável, reproducibilidade, impacto).

---

## Plano por Métrica — Adequação Funcional

### M1 — Cobertura funcional esperada
- **Objetivo:** verificar presença/acessebilidade das funções essenciais (agendar, reagendar, cancelar, integrar, notificar).
- **Passos:**
  1. Listar as funções essenciais esperadas (usar lista da Fase 2).
  2. Navegar/inspecionar a aplicação e confirmar presença e acesso a cada função.
  3. Para cada função encontrada: capturar screenshot da UI e anotar o caminho/menu usado.
- **Entrada:** lista de funções esperadas.  
- **Saída:** número de funções implementadas.  
- **Evidência:** screenshots + descrição do caminho.  
- **Cálculo:** (implementadas ÷ esperadas) × 100.  
- **Julgamento:** aplicar faixas da Fase 2.

---

### M2 — Taxa de sucesso em execução de funcionalidades principais
- **Objetivo:** medir confiabilidade das operações essenciais.
- **Passos:**
  1. Definir 1 caso de teste por funcionalidade principal.
  2. Executar cada caso **3 vezes** (por definição da métrica).
  3. Registrar resultado `Sucesso/Parcial/Falha` e capturar evidências (screenshot ou log).
- **Entrada:** casos de teste.  
- **Saída:** nº de execuções bem-sucedidas / total.  
- **Cálculo:** (execuções bem-sucedidas ÷ total de execuções) × 100.  
- **Evidência:** prints e logs por execução.  
- **Julgamento:** usar faixas da Fase 2.

---

### M3 — Taxa de sucesso dos fluxos de agendamento (5 testes completos)
- **Objetivo:** verificar fluxos ponta-a-ponta: criar, editar, reagendar, cancelar, excluir.
- **Passos:**
  1. Montar 5 casos de fluxo (cada fluxo deve cobrir os passos listados).
  2. Executar cada fluxo uma vez por execução planejada (repetições conforme necessidade de confiabilidade).
  3. Registrar resultado do fluxo inteiro (`Sucesso` somente se todas as etapas funcionarem).
- **Entrada:** 5 casos de fluxo completos.  
- **Saída:** nº de fluxos inteiros bem-sucedidos ÷ total testados.  
- **Evidência:** sequência de screenshots por etapa + logs de sincronização (se aplicável).  
- **Cálculo e julgamento:** conforme fórmula e faixas definidas.

---

### M4 — Ocorrência de erros visíveis durante o agendamento
- **Objetivo:** contar mensagens de erro/falhas visíveis durante os testes funcionais.
- **Passos:**
  1. Durante as execuções de M2/M3, anotar toda mensagem de erro visível (texto, código, passo onde ocorreu).
  2. Capturar screenshot do erro e coletar log relacionado (se houver).
- **Entrada:** execuções de testes.  
- **Saída:** contador de erros por avaliador e por fluxo.  
- **Evidência:** screenshots+logs.  
- **Julgamento:** aplicar faixas de julgamento e listar os erros recorrentes.

---

### M5 — Percentual de funcionalidades esperadas ausentes
- **Objetivo:** identificar lacunas em relação a um produto de referência.
- **Passos:**
  1. Definir lista de funcionalidades de referência (ex.: Calendly — usar lista curta e justificável).
  2. Para cada item, checar se existe funcionalidade no Cal.com; anotar `Presente/ Ausente/ Parcial`.
- **Entrada:** lista de referência.  
- **Saída:** % ausentes.  
- **Evidência:** evidência para cada item (UI/feature flag/documentação).  
- **Cálculo e julgamento:** aplicar fórmula e critérios.

---

### M6 — Número de funcionalidades redundantes identificadas
- **Objetivo:** detectar duplicações funcionais.
- **Passos:**
  1. Explorar menus e fluxos procurando ações com o mesmo propósito.
  2. Para cada duplicidade: documentar ambos os pontos com screenshots e explicar por que se trata de redundância.
- **Entrada:** exploração funcional.  
- **Saída:** contador de redundâncias.  
- **Evidência:** screenshots lado a lado + descrição.  
- **Julgamento:** aplicar faixas.

---

### M7 — Avaliação de impacto percebido pelos avaliadores
- **Objetivo:** medir o impacto subjetivo de ausências/redundâncias.
- **Passos:**
  1. Para cada ausência/redundância encontrada, atribuir nota 1–5 (1 = sem impacto, 5 = muito impacto).
  2. Calcular média das notas.  
- **Entrada:** lista de problemas identificados.  
- **Saída:** nota média de impacto.  
- **Evidência:** formulário de avaliação preenchido por avaliador.  
- **Julgamento:** aplicar faixas da Fase 2.

---

## Plano por Métrica — Portabilidade

### M1 — Taxa de sucesso de instalação em múltiplos ambientes
- **Objetivo:** validar se o software pode ser instalado corretamente em multiplos ambientes.
- **Passos:**
  1. Seguir instruções oficiais de instalação em pelo menos N ambientes distintos (definir N internamente).
  2. Registrar para cada tentativa: sucesso/erro, ponto de falha e logs.  
- **Entrada:** documentação oficial e ambiente de instalação.  
- **Saída:** % instalações bem-sucedidas.  
- **Evidência:** logs de instalação + screenshot do sistema em funcionamento.  
- **Cálculo/julgamento:** conforme faixas da Fase 2.

---

### M2 — Tempo médio estimado de implantação
- **Objetivo:** medir o tempo até o sistema entrar em funcionamento.
- **Passos:**
  1. Para cada instalação (M1), medir tempo total (início → aplicação acessível).
  2. Registrar tempos e calcular média.  
- **Entrada:** medições de tempo reais.  
- **Saída:** tempo médio.  
- **Evidência:** timestamps + logs.  
- **Julgamento:** comparar com limites (≤30 min, 31–60, >60).

---

### M3 — Qualidade percebida da documentação de instalação
- **Objetivo:** avaliar clareza/completude (nota 1–5).
- **Passos:**
  1. Após tentar instalar, cada avaliador atribui nota e comentários sobre lacunas.  
- **Entrada:** experiência de instalação.  
- **Saída:** média de notas e comentários qualitativos.  
- **Evidência:** formulário preenchido.

---

### M4 — Esforço de implantação percebido
- **Objetivo:** medir esforço cognitivo/técnico (1–5).
- **Passos:**
  1. Cada avaliador classifica o esforço (1 = muito fácil, 5 = muito difícil) e descreve passos críticos que demandaram esforço.  
- **Entrada:** experiência de instalação.  
- **Saída:** média de notas e comentários qualitativos.  
- **Evidência:** formulário preenchido.

---

### M5 — Compatibilidade entre navegadores
- **Objetivo:** verificar que fluxos principais funcionam sem erro nos navegadores-alvo.
- **Passos:**
  1. Executar os mesmos fluxos principais (criar, reagendar, cancelar) em cada navegador.  
  2. Registrar `Sucesso/Parcial/Falha` e evidências.  
- **Entrada:** casos de teste padronizados.  
- **Saída:** % fluxos sem erro por navegador.  
- **Evidência:** screenshots por navegador e logs JS/network (se aplicável).  
- **Julgamento:** usar faixas da Fase 2.

---

### M6 — Compatibilidade entre dispositivos
- **Objetivo:** verificar funcionalidade/legibilidade em desktop/mobile(ou emulador).
- **Passos:**
  1. Executar fluxos principais em cada categoria de dispositivo.  
  2. Registrar erros de funcionalidade ou degradação de interface.  
- **Evidência:** screenshots em cada dimensão de tela.  
- **Cálculo/julgamento:** conforme Fase 2.

---

### M7 — Clareza e autonomia na configuração das dependências externas
- **Objetivo:** avaliar se dependências (DB, e-mail, APIs) podem ser configuradas seguindo a documentação sem necessidade de suporte ou ajuda de terceiros.
- **Passos:**
  1. Tentar configurar ao menos um serviço externo (ex.: envio de e-mail) seguindo documentação.  
  2. Registrar passos que exigiram pesquisa/ajuda externa.  
- **Evidência:** logs de configuração + notas sobre gaps na doc.  
- **Julgamento:** nota 1–5 conforme critérios.

---

## Consolidação, Análise e Julgamento (após execução de todas as métricas)
1. **Consolidação:** agregar todas as linhas das planilhas em uma aba mestre.  
2. **Cálculo automático:** usar fórmulas para cada métrica (pré-configuradas na planilha) para obter percentuais e médias.  
3. **Classificação final por métrica:** aplicar faixas (Excelente/Boa/Regular/Insatisfatória) já definidas.  
4. **Síntese por característica:** computar score agregado para *Adequação Funcional* e *Portabilidade* (ex.: média ponderada das métricas; pesos definidos na Fase 2 ou assumir pesos iguais se não definidos).  
5. **Registro de problemas críticos:** listar testes que falharam com evidências e passos para reproduzir.  
6. **Recomendações:** para métricas abaixo do aceitável, indicar causa provável e ação corretiva sugerida.  
7. **Relatório final:** incluir objetivo, método, tabelas de métricas, gráficos simples (percentual de conformidade) e anexos com evidências.

---

## Critérios de aceitação globais (aplicáveis ao relatório)
- Todas as métricas possuem evidência anexada (screenshot ou log).  
- Todas as métricas foram calculadas e comparadas com critérios da Fase 2.  
- Resultados não ambíguos: cada métrica tem resultado classificado como `Atende / Parcial / Não atende`.  
- O relatório indica claramente quais problemas são críticos e quais são de baixa prioridade.

---
