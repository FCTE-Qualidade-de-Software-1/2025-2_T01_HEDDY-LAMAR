# Fase 4 — Execução e Resultados da Avaliação

## 1. Introdução
Nesta fase, foram executados os procedimentos definidos no **Plano de Avaliação (Fase 3)**. O objetivo foi coletar evidências objetivas sobre a **Adequação Funcional** do software **Cal.com**, 

Todos os testes foram realizados em ambiente controlado, respeitando os critérios de reprodutibilidade e transparência.

## 2. Ambiente de Execução

Os testes foram realizados conforme as especificações abaixo:

| Item | Detalhe |
| :--- | :--- |
| **Versão do Software** | Cal.com (Versão Web/SaaS Atual) |
| **Navegador** | Google Chrome (Latest Version) |
| **Sistema Operacional** | Windows 11 |
| **Ferramentas de Apoio** | Software de captura de tela e gravação de vídeo (OBS/Loom) |

---

## 3. Resultados por Métrica

### 3.1. Resultado da Métrica M1 — Cobertura Funcional Esperada

**Objetivo:** Verificar a presença das funções essenciais.

#### 3.1.1. Registro de Execução

| ID | Funcionalidade | Status | Evidência |
| :--- | :--- | :--- | :--- |
| **M1-01** | Criar novo tipo de evento | ✅ Presente | [M1-01_Criar.png](https://drive.google.com/drive/folders/1n-DDD9UCLmzwpaADYoO_bqiENyFlbl5r?usp=drive_link)|
| **M1-02** | Editar detalhes do evento | ✅ Presente | [M1-02_Editar.png](https://drive.google.com/drive/folders/1VBEWrAvBR7I-hogWlgOBFdYNS57GN-GO?usp=drive_link) |
| **M1-03** | Excluir tipos de evento | ✅ Presente | [M1-03_Excluir.png](https://drive.google.com/drive/folders/18OJZ1SVc6JpWMNG4bmNMo9P_icNke74U?usp=drive_link)  |
| **M1-04** | Reagendar compromisso | ✅ Presente | [M1-04_Reagendar.png](https://drive.google.com/drive/folders/1YZvZ13LP5s02pO7b_XEfeq_zVcpWTjXQ?usp=drive_link)  |
| **M1-05** | Integrar com Google Calendar | ✅ Presente | [M1-05_Integrar.png](https://drive.google.com/drive/folders/1MEBK5A1QscfWQPwQD8rCsB2E7Sux7Btv?usp=drive_link)  |
| **M1-06** | Notificar (E-mail automático) | ✅ Presente | [M1-06_Notificar.png](https://drive.google.com/drive/folders/1SOvO3cSfK7Hw84-w_5EFFW2cWGt4tWur?usp=drive_link)  |

#### 3.1.2. Cálculo e Análise
* **Funções Esperadas:** 6
* **Funções Implementadas:** 6

$$Resultado (M1) = \left( \frac{6}{6} \right) \times 100 = 100\%$$

"Julgamento M1: Excelente"
    O software apresentou 100% de cobertura das funcionalidades essenciais listadas, enquadrando-se no critério **Excelente (≥90%)**.

---

### 3.2. Resultado da Métrica M2 — Taxa de Sucesso em Execução

**Objetivo:** Medir a confiabilidade na execução repetida de uma funcionalidade crítica.
**Cenário de Teste:** Criação de um Evento (Executado 3 vezes).

#### 3.2.1. Registro de Execução

| ID Exec | Cenário | Resultado | Evidência (Vídeo) |
| :--- | :--- | :--- | :--- |
| **EXEC-M2-01** | Criação de Evento (Tentativa 1) | ✅ Sucesso | [M2.mp4](https://drive.google.com/drive/folders/1CSf5iS7yHkFTktySnGiUMMKj0or46Q2f?usp=drive_link) |
| **EXEC-M2-02** | Criação de Evento (Tentativa 2) | ✅ Sucesso | [M2.mp4](https://drive.google.com/drive/folders/1CSf5iS7yHkFTktySnGiUMMKj0or46Q2f?usp=drive_link) |
| **EXEC-M2-03** | Criação de Evento (Tentativa 3) | ✅ Sucesso | [M2.mp4](https://drive.google.com/drive/folders/1CSf5iS7yHkFTktySnGiUMMKj0or46Q2f?usp=drive_link)|

#### 3.2.2. Cálculo e Análise
* **Total de Execuções:** 3
* **Execuções com Sucesso:** 3

$$Resultado (M2) = \left( \frac{3}{3} \right) \times 100 = 100\%$$

"Julgamento M2: Excelente"
    A funcionalidade demonstrou estabilidade total nas repetições, atingindo o critério **Excelente (≥95%)**.

---

### 3.3. Resultado da Métrica M3 — Taxa de Sucesso dos Fluxos (Ponta a Ponta)

**Objetivo:** Verificar o ciclo de vida completo do agendamento.
**Fluxo Testado:** Criar $\rightarrow$ Editar $\rightarrow$ Reagendar $\rightarrow$ Cancelar $\rightarrow$ Excluir.

#### 3.3.1. Registro de Execução

| ID Exec | Cenário | Resultado | Evidência (Vídeo) |
| :--- | :--- | :--- | :--- |
| **EXEC-M3-01** | Fluxo Completo #1 | ✅ Sucesso | [Video_M3_Fluxo.mp4](https://drive.google.com/drive/folders/1oKXbdFQVbsF3nunTa_ZbtoNguf813XIc?usp=drive_link) |
| **EXEC-M3-02** | Fluxo Completo #2 | ✅ Sucesso | [Video_M3_Fluxo.mp4](https://drive.google.com/drive/folders/1oKXbdFQVbsF3nunTa_ZbtoNguf813XIc?usp=drive_link) |
| **EXEC-M3-03** | Fluxo Completo #3 | ✅ Sucesso | [Video_M3_Fluxo.mp4](https://drive.google.com/drive/folders/1oKXbdFQVbsF3nunTa_ZbtoNguf813XIc?usp=drive_link) |
| **EXEC-M3-04** | Fluxo Completo #4 | ✅ Sucesso | [Video_M3_Fluxo.mp4](https://drive.google.com/drive/folders/1oKXbdFQVbsF3nunTa_ZbtoNguf813XIc?usp=drive_link) |
| **EXEC-M3-05** | Fluxo Completo #5 | ✅ Sucesso | [Video_M3_Fluxo.mp4](https://drive.google.com/drive/folders/1oKXbdFQVbsF3nunTa_ZbtoNguf813XIc?usp=drive_link) |

#### 3.3.2. Cálculo e Análise
* **Fluxos Testados:** 5
* **Fluxos Bem-sucedidos:** 5

$$Resultado (M3) = \left( \frac{5}{5} \right) \times 100 = 100\%$$

"Julgamento M3: Excelente"
    O sistema permitiu realizar todo o ciclo de vida do agendamento sem interrupções ou falhas de integridade em todas as tentativas. Classificação: **Excelente**.

---

### 3.4. Resultado da Métrica M4 — Ocorrência de Erros Visíveis

**Objetivo:** Contabilizar falhas, mensagens de erro ou crashes durante as execuções de M2 e M3.

#### 3.4.1. Registro de Ocorrências

Durante a execução dos testes funcionais e de fluxo (totalizando mais de 8 interações complexas), o monitoramento de erros apresentou o seguinte resultado:

| Tipo de Erro | Quantidade Detectada | Descrição |
| :--- | :---: | :--- |
| **Erros Bloqueantes** | 0 | Nenhum impedimento de fluxo. |
| **Erros Não-Bloqueantes** | 0 | Nenhuma mensagem de alerta indevida. |
| **Erros Cosméticos** | 0 | Interface manteve-se consistente. |
| **TOTAL** | **0** | |

#### 3.4.2. Análise

"Julgamento M4: Excelente"
    Não foram identificadas mensagens de erro (Flash messages, erros 404/500 no console ou travamentos) durante o período de teste.
    **Critério Atingido:** Excelente (0 erros).

---

### 3.5 Portabilidade

#### 3.5.1. Resultado da Métrica M1 — Taxa de Sucesso de Instalação em Múltiplos Ambientes

#### 3.5.2. Resultado da Métrica M2 — Tempo Médio Estimado de Implantação

#### 3.5.3. Resultado da Métrica M3 — Qualidade Percebida da Documentação de Instalação

#### 3.5.4. Resultado da Métrica M4 — Esforço de Implantação Percebido

#### 3.5.5. Resultado da Métrica M5 — Compatibilidade Entre Navegadores

**Objetivo:** Validar se os principais fluxos de uso funcionam corretamente e sem erros nos navegadores suportados.

**Navegadores Avaliados:**

- [Mozilla Firefox](https://drive.google.com/drive/folders/1exkM2vTe1Nal6MyOCxa8WnGIWEbHUPQX?usp=sharing)  
- [Google Chrome](https://drive.google.com/drive/folders/1Z0f8OaT-rpCIE8TRl7d0Ezw9cmpXMuVO?usp=sharing) 
- [Microsoft Edge](https://drive.google.com/drive/folders/1qvSvxk2ZVppUILlRiFkekImgGg3GL519?usp=sharing) 

Os testes foram realizados diretamente na plataforma **Cal.com**.

---

### 3.5.5.1. Método de Verificação

Foram analisadas **duas páginas principais** relacionadas a:

- Reuniões  
- Eventos  

Em cada navegador foram executadas ações essenciais do uso do sistema, contemplando:

- Criação de informações  
- Consulta e navegação entre elementos  
- Atualização e reagendamento  
- Cancelamento ou exclusão de registros  

Também foram verificadas as seguintes dimensões técnicas:

- Consistência da interface e comportamento visual
- Funcionamento de recursos dependentes de JavaScript
- Erros visíveis ao usuário
- Registros no console e comportamento de rede

---

### 3.5.5.2. Resultados Observados

Durante os testes:

- A interface permaneceu **coerente e estável** em todos os navegadores.
- Todos os fluxos avaliados foram executados **com sucesso**, sem interrupções ou falhas.
- **Nenhum log de erro foi identificado no console** durante as interações.

---

### 3.5.5.3. Métrica Final

- **Fluxos Testados:** 2
- **Fluxos Bem-sucedidos:** 2

$$Resultado (M5) = \left( \frac{2}{2} \right) \times 100 = 100\%$$

> **Julgamento M5:** **Excelente**  
O sistema apresentou comportamento consistente e funcional em todos os navegadores avaliados, atendendo plenamente aos critérios de compatibilidade.

---

**Entrada:** Casos de teste padronizados  
**Saída:** 100% dos fluxos executados sem erro por navegador  
**Evidências:**  [Capturas de tela e registros técnicos disponíveis no Drive](https://drive.google.com/drive/folders/1548MaV_Aqxt4u7Eh4xjfZ44Y9GKlfbg_?usp=sharing)

---

#### 3.5.6. Resultado da Métrica M6 — Compatibilidade Entre Dispositivos

#### 3.5.7. Resultado da Métrica M7 — Clareza e Autonomia na Configuração das Dependências Externas

## 4. Conclusão da Avaliação Funcional

Com base nos dados coletados na Fase 4, o software **Cal.com** demonstrou um nível elevado de maturidade no quesito **Adequação Funcional**.

| Métrica | Resultado Numérico | Classificação |
| :--- | :---: | :--- |
| **M1 (Cobertura)** | 100% | Excelente |
| **M2 (Confiabilidade)** | 100% | Excelente |
| **M3 (Fluxo Completo)** | 100% | Excelente |
| **M4 (Ausência de Erros)** | 0 erros | Excelente |

**Parecer Final:** O software atende plenamente aos requisitos funcionais estabelecidos para gestão de agendamentos, apresentando robustez tanto em operações isoladas quanto em fluxos complexos de longa duração.


## Histórico de Versões

| Versão | Data       | Descrição                                                               | Autor                               |
| :----- | :--------- | :---------------------------------------------------------------------- | :---------------------------------- |
| `1.0`  | 23/11/2025 | Criação da estrutura inicial da página e adição dos resultados das metricas m1 ao m4 da adequação funcional| [Vinicius Alves](https://github.com/Vinialves2020) |
| `1.1`  | 24/11/2025 | Organizando espaço para métricas de portabilidade | [Antonio Carvalho](https://github.com/antonioscarvalho) |
