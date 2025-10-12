# Fase 02

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
---

## Referências
