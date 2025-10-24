# 1. Especificação da Avaliação

## 1.1. Metodologia **GQM (Goal Question Metric)**

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


<br>


Analisar o software Cal.com, uma plataforma de agendamento open source e auto-hospedável, com o propósito de avaliar sua qualidade quanto às características de Adequação Funcional e Portabilidade, de acordo com o modelo de qualidade ISO/IEC 25010.

A avaliação busca verificar o grau de completude e correção das funcionalidades essenciais de agendamento, bem como a capacidade da aplicação de operar e ser implantada em diferentes ambientes.

A análise é conduzida do ponto de vista dos usuários finais e avaliadores técnicos, considerando o contexto de uso real do sistema, que inclui a integração com calendários externos (como Google Calendar e Outlook), a execução multiplataforma (Linux, Windows e macOS) e o suporte a implantação via self-hosting documentada pela equipe do Cal.com.


---

## 1.2. Métricas (Q)

>Cada questão é associada a métricas que permitem responder de maneira quantitativa e verificável.
>Os dados coletados podem ser:
>- Objetivos: dependem apenas do objeto medido, como número de versões de um artefato, esforço (em horas) despendido em uma tarefa ou tamanho de um módulo de código;
>- Subjetivos: dependem tanto do objeto quanto da percepção do avaliador, como legibilidade de um documento, clareza de uma interface ou nível de satisfação do usuário.
>
>(BASILI et al., 1994, p. 529)

<div align="center">
  <strong>Figura 2 – Descrição das Métricas</strong>
  <br>
  <img src="../assets/GQM/basili_metrics.png" alt="Métricas">
  <br>
  <em>Fonte: Basili et al. (1994, p. 529).</em>
</div>

---

## 1.3. Questões (Q)

>Nesse estágio, um conjunto de questões orienta a forma de avaliação do objetivo definido, descrevendo como e em que medida o objeto será examinado segundo um modelo de qualidade.
>Essas perguntas buscam caracterizar o produto, processo ou recurso em relação a aspectos específicos da qualidade, permitindo compreender seu desempenho sob o ponto de vista selecionado.
>
>(BASILI et al., 1994, p. 528)

<div align="center">
  <strong>Figura 4 – Descrição das Questões</strong>
  <br>
  <img src="../assets/GQM/basili_questions.png" alt="Diagrama GQM com Nível Conceitual, Operacional e Quantitativo">
  <br>
  <em>Fonte: Basili et al. (1994, p. 528).</em>
</div>

---

## 1.4. Objetivos (Goals)

>Neste nível, um objetivo é feito para um determinado objeto de medição, podendo ser analisado sob diferentes perspectivas:
>- Produtos: artefatos e entregáveis gerados ao longo do ciclo de vida do sistema, como especificações, diagramas, código-fonte e casos de teste;
>- Processos: atividades relacionadas ao desenvolvimento de software, como modelagem, codificação, testes e entrevistas;
>- Recursos: elementos utilizados na execução dos processos, como equipe, hardware, software e infraestrutura de apoio.
>
>(BASILI et al., 1994, p. 528)
<br>
<br>
<div align="center">
  <strong>Figura 3 – Descrição dos Objetivos</strong>
  <br>
  <img src="../assets/GQM/basili_goals.png" alt="Objetivos">
  <br>
  <em>Fonte: Basili et al. (1994, p. 528).</em>
</div> 

---

## 1.5. Escopo da Avaliação

| **Elemento** | **Descrição** |
| :------------ | :------------- |
| **O que será avaliado** | O sistema **Cal.com** (versão open source estável disponível no GitHub até outubro de 2025), com foco nos módulos de **agendamento de eventos**, **integração com calendários externos** (Google Calendar, Outlook) e **envio de notificações**. |
| **O que não será avaliado** | Aspectos relacionados à **segurança da informação**, **desempenho do sistema** e **usabilidade da interface**, que serão abordados em etapas futuras do projeto. |
| **Ambiente de teste e condições** | Testes realizados em ambiente controlado, com os seguintes parâmetros:<br>• **Sistemas Operacionais:** Ubuntu 22.04, Windows 11 e macOS Sonoma<br>• **Navegadores:** Google Chrome, Mozilla Firefox e Safari<br>• **Dispositivos:** Desktop e notebook<br>• **Conexão:** Internet banda larga estável |
| **Responsáveis e papéis** | • **Equipe de Avaliação:** autores do projeto (Antonio Carvalho, Gustavo Haubert, Atyrson Souto, Vinicius Alves, Cairo Florenço e Pedro Henrique Braga de Morais)<br>• **Orientação e supervisão:** Profa. **Cristiane Soares Ramos**<br>• **Responsáveis pela coleta e interpretação de métricas:** Equipe de desenvolvimento e avaliadores de qualidade |

---

## Links para as páginas dos nossos artefatos GQM:

- [1° Objetivo de Medição: Adequação Funcional](../fase_2/obj_adequacao_funcional.md)  
- [2° Objetivo de Medição: Portabilidade](../fase_2/obj_portabilidade.md)

---

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
| `1.9`  | 21/10/2025 | Adiciona novas métricas de portabilidade e adiciona critérios de julgamento nas duas tabelas  | [Cairo Florenço](https://github.com/CA1RO) |
| `2.0`  | 23/10/2025 | Padronização de artefatos e tabelas de acordo com estruturação hierárquica de objetivo, questões e métricas, juntamente da adição de novos conceitos e suas respectivas referências | [Antonio Carvalho](https://github.com/antonioscarvalho) |
| `2.1`  | 23/10/2025 | Criação de estruturação mais adequada com separação de artefatos | [Antonio Carvalho](https://github.com/antonioscarvalho) |

## Referências

SILVA, Carlos Vinícius Pereira da; MOURA, Déborah Carvalho de; CAMPOS, Danylo de Castro; NERY, Paulo. *GQM: Goal - Question - Metric*. 2009.

CAL.COM. *About Cal.com, Inc. Connecting a billion people by 2031*. Disponível em: https://cal.com/about. Acesso em: 23 out. 2025.

BASILI, Victor R.; CALDIERA, Gianluigi; ROMBACH, H. Dieter. *Goal Question Metric Paradigm*. In: MARCINIAK, John J. (Ed.). Encyclopedia of Software Engineering - 2° Vol. New York: John Wiley & Sons, Inc., 1994. P. 528, 529. 
