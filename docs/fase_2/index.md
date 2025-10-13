# Especificação da Avaliação

## Metodologia **GQM (Goal Question Metric)**

Para a realização da etapa de especificação da avaliação utilizaremos a metodologia GQM.

> GQM é uma abordagem de cima para baixo (top-down) para estabelecer um sistema de medição direcionado a metas para o desenvolvimento de software, em que a equipe começa com metas organizacionais, define a medição das metas, levanta questões a abordar os objetivos e identifica as métricas que proporcionem respostas às perguntas.
>
> (SILVA et al., 2009, p. 4)

<div align="center">
  <strong>Figura 1 – Definição das Métricas GQM</strong>
  <br>
  <img src="../assets/gqm_diagrama.png" alt="Diagrama GQM com Nível Conceitual, Operacional e Quantitativo">
  <br>
  <em>Fonte: Silva et al. (2009, p. 4).</em>
</div>

## Objetivo Geral (Goal)

Avaliar a qualidade do software Cal.com, um sistema open source de agendamento, considerando as características Adequação Funcional e Portabilidade, conforme o modelo de qualidade ISO/IEC 25010. O propósito é verificar se o sistema atende corretamente às necessidades funcionais dos usuários e se apresenta facilidade de instalação, execução e adaptação em diferentes ambientes.

### Objetivos Específicos

1. Verificar se as funcionalidades implementadas no Cal.com atendem aos requisitos funcionais esperados pelos usuários e administradores.

2. Avaliar o comportamento e a completude das funcionalidades principais do sistema (criação de eventos, integração com calendários, envio de notificações).

3. Analisar a capacidade de portabilidade do sistema, considerando sua adaptabilidade a diferentes sistemas operacionais, navegadores e ambientes de execução.

4. Medir o esforço necessário para instalar e configurar o Cal.com em diferentes contextos e identificar dependências que impactem sua portabilidade.

## Escopo da Avaliação

| **Elemento** | **Descrição** |
| :------------ | :------------- |
| **O que será avaliado** | O sistema **Cal.com** (versão open source estável disponível no GitHub até outubro de 2025), com foco nos módulos de **agendamento de eventos**, **integração com calendários externos** (Google Calendar, Outlook) e **envio de notificações**. |
| **O que não será avaliado** | Aspectos relacionados à **segurança da informação**, **desempenho do sistema** e **usabilidade da interface**, que serão abordados em etapas futuras do projeto. |
| **Ambiente de teste e condições** | Testes realizados em ambiente controlado, com os seguintes parâmetros:<br>• **Sistemas Operacionais:** Ubuntu 22.04, Windows 11 e macOS Sonoma<br>• **Navegadores:** Google Chrome, Mozilla Firefox e Safari<br>• **Dispositivos:** Desktop e notebook<br>• **Conexão:** Internet banda larga estável |
| **Responsáveis e papéis** | • **Equipe de Avaliação:** autores do projeto (Gustavo Haubert, Atyrson Souto, Vinicius Alves e Cairo Florenço)<br>• **Orientação e supervisão:** Profa. **Cristiane Soares Ramos**<br>• **Responsáveis pela coleta e interpretação de métricas:** Equipe de desenvolvimento e avaliadores de qualidade |


## Questões (Questions)

### Adequação Funcional

1. As funcionalidades principais do sistema (agendamento, notificação e integração com Google Calendar, Outlook, etc.) estão implementadas conforme os requisitos esperados?  
2. As funcionalidades executam suas tarefas corretamente, sem falhas perceptíveis pelo usuário?  
3. Existem funcionalidades redundantes ou ausentes que prejudiquem a experiência do usuário?  
4. O comportamento do sistema é consistente em diferentes cenários de uso?

### Portabilidade

1.  O sistema pode ser instalado e executado em diferentes sistemas operacionais (Linux, macOS, Windows)?
2.  O Cal.com apresenta o mesmo comportamento em diferentes navegadores e dispositivos móveis?
3.  O processo de instalação e configuração é simples e bem documentado?
4.  Existem dependências externas que dificultam a implantação do sistema em novos ambientes?


## Métricas (Metrics)

### Adequação Funcional

| **Código** | **Métrica** | **Tipo** | **Descrição** |
|-------------|--------------|-----------|----------------|
| **M1** | Percentual de requisitos funcionais implementados | Quantitativa | (Nº de requisitos implementados ÷ Nº total de requisitos) × 100 |
| **M2** | Taxa de sucesso em testes funcionais | Quantitativa | (Nº de testes aprovados ÷ Nº total de testes executados) × 100 |
| **M3** | Número de falhas funcionais registradas por release | Quantitativa | Contagem de issues de falhas funcionais abertas/fechadas |
| **M4** | Grau de consistência funcional | Qualitativa | Avaliação baseada na observação de comportamento uniforme das funções |


### Portabilidade

| **Código** | **Métrica** | **Tipo** | **Descrição** |
|------------|-------------|----------|---------------|
| **M5** | Taxa de sucesso de instalação em múltiplos ambientes | Quantitativa | (Nº de instalações bem-sucedidas ÷ Nº total de tentativas) × 100 |
| **M6** | Tempo médio de implantação | Quantitativa | Tempo em minutos/horas para instalar e configurar o sistema |
| **M7** | Número de incompatibilidades identificadas entre plataformas | Quantitativa | Quantidade de falhas registradas em diferentes SOs ou navegadores |
| **M8** | Grau de dependência tecnológica | Qualitativa | Classificação (baixa, média ou alta) com base na análise das dependências externas |


## Histórico de Versões

| Versão | Data       | Descrição                                                               | Autor                               |
| :----- | :--------- | :---------------------------------------------------------------------- | :---------------------------------- |
| `1.0`  | 12/10/2025 | Criação da estrutura inicial da página e criação das questões e métricas da adequação funcional | [Gustavo Haubert](https://github.com/GustavoHaubert) |
| `1.1`  | 12/10/2025 | Criação das questões e métricas de portabilidade | [Atyrson Souto](https://github.com/Atyrson) |
| `1.2`  | 12/10/2025 | Criação dos Objetivos | [Vinicius Alves](https://github.com/vinialves2020) |
| `1.3`  | 12/10/2025 | Adicionando tópico sobre a metodologia | [Cairo Florenço](https://github.com/CA1RO) |
| `1.4`  | 12/10/2025 | Adicionando tabela de escopo | [Antonio Carvalho](https://github.com/antonioscarvalho) |

## Referências

SILVA, Carlos Vinícius Pereira da; MOURA, Déborah Carvalho de; CAMPOS, Danylo de Castro; NERY, Paulo. GQM: Goal - Question - Metric. 2009.
