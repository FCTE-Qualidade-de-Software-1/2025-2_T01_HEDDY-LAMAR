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

## Objetivo (Goal)

Analisar o software Cal.com com o propósito de avaliar sua qualidade, com respeito às características Adequação Funcional e Portabilidade, do ponto de vista dos usuários, no contexto do modelo de qualidade ISO/IEC 25010.

## Escopo da Avaliação

| **Elemento** | **Descrição** |
| :------------ | :------------- |
| **O que será avaliado** | O sistema **Cal.com** (versão open source estável disponível no GitHub até outubro de 2025), com foco nos módulos de **agendamento de eventos**, **integração com calendários externos** (Google Calendar, Outlook) e **envio de notificações**. |
| **O que não será avaliado** | Aspectos relacionados à **segurança da informação**, **desempenho do sistema** e **usabilidade da interface**, que serão abordados em etapas futuras do projeto. |
| **Ambiente de teste e condições** | Testes realizados em ambiente controlado, com os seguintes parâmetros:<br>• **Sistemas Operacionais:** Ubuntu 22.04, Windows 11 e macOS Sonoma<br>• **Navegadores:** Google Chrome, Mozilla Firefox e Safari<br>• **Dispositivos:** Desktop e notebook<br>• **Conexão:** Internet banda larga estável |
| **Responsáveis e papéis** | • **Equipe de Avaliação:** autores do projeto (Antonio Carvalho, Gustavo Haubert, Atyrson Souto, Vinicius Alves, Cairo Florenço e Pedro Henrique Braga de Morais)<br>• **Orientação e supervisão:** Profa. **Cristiane Soares Ramos**<br>• **Responsáveis pela coleta e interpretação de métricas:** Equipe de desenvolvimento e avaliadores de qualidade |

## Questões (Questions)

### Adequação Funcional

1. As funcionalidades principais do sistema (agendamento, notificação e integração com Google Calendar, Outlook, etc.) estão implementadas conforme o esperado para um software de agendamento?
    - **Hipótese:** Acredita-se que o Cal.com implementa a maioria das funcionalidades essenciais para um sistema de agendamento, atendendo aos requisitos esperados para um produto de sua categoria.
2. As funções centrais de agendamento (criação, edição, cancelamento e reagendamento) funcionam corretamente e de forma previsível?
    - **Hipótese:** Espera-se que as funcionalidades principais de agendamento operem corretamente na maioria dos cenários, embora possam existir falhas menores que não comprometam a experiência do usuário de forma crítica.
3. Existem funcionalidades redundantes ou ausentes?
    - **Hipótese:** A hipótese é de que o sistema possui as funcionalidades adequadas para seu propósito, sem redundâncias significativas. No entanto, podem ser identificadas oportunidades de melhoria ou a ausência de funcionalidades secundárias.
4. Qual o nível de impacto de funcionalidades ausentes ou redundantes para o uso do sistema?
    - **Hipótese:** Supõe-se que a ausência de funcionalidades secundárias pode impactar a experiência de usuários avançados, mas não deve prejudicar o fluxo principal de agendamento para o usuário comum.
5. Qual o nível de consistência do uso do software entre diferentes navegadores e sessões?
    - **Hipótese:** Espera-se que o sistema mantenha um comportamento consistente, garantindo que as ações do usuário resultem em respostas previsíveis e uniformes na maioria dos cenários de uso.

### Portabilidade

1. O processo de *self-hosting* (auto-hospedagem) do Cal.com é bem documentado e pode ser executado com sucesso em diferentes ambientes de servidor (ex: Docker, Vercel, provedores de nuvem)?
    - **Hipótese:** Acredita-se que a documentação oficial fornece um guia claro para a implantação, permitindo que usuários com conhecimento técnico moderado realizem o *self-hosting* com sucesso.
2. A aplicação web do Cal.com mantém sua funcionalidade e aparência consistentes quando acessada a partir de diferentes navegadores (Chrome, Firefox, Safari)?
    - **Hipótese:** Espera-se que a aplicação seja totalmente funcional e consistente nos principais navegadores, com possíveis variações visuais mínimas que não afetem a usabilidade.
3. O esforço necessário para configurar e implantar uma instância própria do Cal.com é considerado baixo?
    - **Hipótese:** A hipótese é de que o esforço de implantação é baixo para ambientes baseados em Docker, mas pode ser moderado em configurações de servidor mais tradicionais que exigem gerenciamento manual de dependências.
4. As dependências de infraestrutura (banco de dados, variáveis de ambiente, etc.) necessárias para a implantação estão claramente especificadas e são de fácil gerenciamento?
    - **Hipótese:** Supõe-se que as dependências críticas estão bem documentadas, mas a configuração de serviços externos (como provedores de e-mail) pode exigir um esforço adicional.


## Métricas (Metrics)

### Adequação Funcional

| **Código** | **Métrica** | **Tipo** | **Descrição** |
|-------------|--------------|-----------|----------------|
| **M1** | Cobertura funcional esperada | Quantitativa | Verificar quantas funcionalidades essenciais (agendar, reagendar, cancelar, integrar, notificar) estão implementadas e acessíveis. <br>(Nº funcionalidades implementadas ÷ Nº esperadas) × 100 |
| **M2** | Taxa de sucesso em execução de funcionalidades principais | Quantitativa | Executar cada funcionalidade principal ao menos 3 vezes e calcular. <br>(Execuções bem-sucedidas ÷ Total de execuções) × 100 |
| **M3** | Taxa de sucesso dos fluxos de agendamento | Quantitativa | Realizar 5 testes completos (criar, editar, reagendar, cancelar). <br>(Fluxos bem-sucedidos ÷ Total de testes) × 100 |
| **M4** | Ocorrência de erros visíveis durante o agendamento | Quantitativa | Contar mensagens de erro, falhas na interface ou inconsistências em cada teste funcional. |
| **M5** |Percentual de funcionalidades esperadas ausentes | Quantitativa | Identificar funcionalidades essenciais em outras aplicações de agendamento mas não encontradas na aplicação. <br>(Ausentes ÷ Esperadas) × 100 |
| **M6** |Número de funcionalidades redundantes identificadas | Quantitativa | Contar funções que duplicam propósitos (ex.: dois modos diferentes de cancelar o mesmo evento).|
| **M7** |Avaliação de impacto percebido pelos avaliadores | Qualitativa | Atribuir notas de 1 ( sem impacto) a 5 (muito impacto) para cada função ausente ou redundante e calcular a média.|
| **M8** |Compatibilidade entre navegadores | Quantitativa | Executar fluxos idênticos para cada navegador (criar, cancelar, reagendar) nos navegadores Chrome, Firefox e Safari. <br>(Fluxos sem erro ÷ Total) × 100|


### Portabilidade

| **Código** | **Métrica** | **Tipo** | **Descrição** |
|------------|-------------|----------|---------------|
| **M9** | Taxa de sucesso de instalação em múltiplos ambientes | Quantitativa | (Nº de instalações bem-sucedidas ÷ Nº total de tentativas) × 100 |
| **M10** | Tempo médio de implantação | Quantitativa | Tempo em minutos/horas para instalar e configurar o sistema |
| **M11** | Número de incompatibilidades (Funcionais e Visuais) | Quantitativa | Contagem de falhas funcionais ou quebras de layout significativas registradas em diferentes SOs ou navegadores. |
| **M12** | Qualidade Percebida da Documentação | Qualitativa | Avaliação (escala 1-5) atribuída pela equipe sobre a clareza, completude e precisão da documentação de self-hosting e configuração de dependências. |
| **M13** | Percepção de Esforço de Implantação | Qualitativa | Avaliação (escala 1-5) do esforço (cognitivo e técnico) percebido pela equipe para concluir a instalação, mesmo seguindo a documentação. |


## Histórico de Versões

| Versão | Data       | Descrição                                                               | Autor                               |
| :----- | :--------- | :---------------------------------------------------------------------- | :---------------------------------- |
| `1.0`  | 12/10/2025 | Criação da estrutura inicial da página e criação das questões e métricas da adequação funcional | [Gustavo Haubert](https://github.com/GustavoHaubert) |
| `1.1`  | 12/10/2025 | Criação das questões e métricas de portabilidade | [Atyrson Souto](https://github.com/Atyrson) |
| `1.2`  | 12/10/2025 | Criação dos Objetivos | [Vinicius Alves](https://github.com/vinialves2020) |
| `1.3`  | 12/10/2025 | Adicionando tópico sobre a metodologia | [Cairo Florenço](https://github.com/CA1RO) |
| `1.4`  | 12/10/2025 | Adicionando tabela de escopo | [Antonio Carvalho](https://github.com/antonioscarvalho) |
| `1.5` | 20/10/2025 | Reformula o Objetivo da avaliação de acordo com a GQM após feedback da professora | [Pedro Braga](https://github.com/Stain19) |
| `1.6` | 20/10/2025 | Adiciona hipóteses para cada pergunta de adequação funcional e portabilidade, além de reformular as perguntas de portabilidade | [Pedro Braga](https://github.com/Stain19) |
| `1.7` | 21/10/2025 | Refina as métricas de portabilidade, desmembrando a métrica M8 para melhor adequação às questões | [Atyrson Souto](https://github.com/Atyrson) |
| `1.8`  | 21/10/2025 | Ajuste nas questões de adequação funcional e suas métricas  | [Gustavo Haubert](https://github.com/GustavoHaubert) |

## Referências

SILVA, Carlos Vinícius Pereira da; MOURA, Déborah Carvalho de; CAMPOS, Danylo de Castro; NERY, Paulo. GQM: Goal - Question - Metric. 2009.
