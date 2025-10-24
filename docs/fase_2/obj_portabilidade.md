## 2° Objetivo de Medição: Portabilidade

| Elemento | Descrição |
| :-- | :-- |
| **Analisar** | o software **Cal.com** |
| **Para o propósito de** | avaliar sua qualidade quanto à capacidade de ser instalado, executado e utilizado em diferentes ambientes |
| **Com respeito a** | **Portabilidade** |
| **Do ponto de vista de** | **usuários e avaliadores técnicos** |
| **No contexto de** | **avaliação da qualidade de software segundo o modelo ISO/IEC 25010** |

**Tabela 1 – 2° Objetivo de Medição: Portabilidade**

---

#### Q1 – Documentação de Self-Hosting
O processo de *self-hosting* (auto-hospedagem) do Cal.com é bem documentado e pode ser executado com sucesso em diferentes ambientes de servidor?

- **Hipót. H1.1:** A documentação oficial fornece um guia claro para implantação, permitindo que usuários com conhecimento técnico moderado realizem o *self-hosting* com sucesso.

---

#### Q2 – Consistência Entre Navegadores
A aplicação web do Cal.com mantém sua funcionalidade e aparência consistentes quando acessada a partir de diferentes navegadores?

- **Hipót. H2.1:** A aplicação é totalmente funcional e consistente nos principais navegadores, com variações visuais mínimas que não afetam a usabilidade.

---

#### Q3 – Esforço de Implantação
O esforço necessário para configurar e implantar uma instância própria do Cal.com é considerado baixo?

- **Hipót. H3.1:** O esforço de implantação é baixo em ambientes baseados em Docker, mas moderado em configurações que exigem gerenciamento manual de dependências.

---

#### Q4 – Dependências de Infraestrutura
As dependências de infraestrutura necessárias para a implantação estão claramente especificadas e são de fácil gerenciamento?

- **Hipót. H4.1:** As dependências críticas estão bem documentadas, mas a configuração de serviços externos (como provedores de e-mail) pode exigir esforço adicional.

---

#### Q5 – Compatibilidade Entre Dispositivos
A interface e as funcionalidades do Cal.com permanecem acessíveis e utilizáveis em diferentes dispositivos?

- **Hipót. H5.1:** O design responsivo da aplicação mantém todas as principais funcionalidades operacionais e legíveis em qualquer dispositivo, sem perda significativa de usabilidade.

---

### Métricas Relacionadas

| **Código** | **Métrica** | **Tipo** | **Descrição** | **Critério de Julgamento** |
|:--:|:--|:--|:--|:--|
| **M9** | Taxa de sucesso de instalação em múltiplos ambientes | Quantitativa | Verificar, com base na documentação, se o processo de instalação pode ser realizado em diferentes sistemas. <br>**Fórmula:** (Instalações bem documentadas ÷ Total de ambientes descritos) × 100 | ≥ 90% = Excelente <br>70–89% = Regular <br><70% = Insatisfatória |
| **M10** | Tempo médio estimado de implantação | Quantitativa | Estimar o tempo total descrito na documentação para preparar o ambiente e executar o sistema até o funcionamento pleno. <br>**Fórmula:** (∑ tempos estimados ÷ nº de ambientes) | ≤ 30 min = Excelente <br>31–60 = Regular <br>>60 = Precisa de otimização |
| **M11** | Qualidade percebida da documentação de instalação | Qualitativa | Avaliar (escala 1–5) a clareza, completude e precisão da documentação. Média das notas dos avaliadores. | ≥ 4,5 = Excelente <br>3–4,4 = Boa <br> < 3 = Fraca |
| **M12** | Esforço de implantação percebido pela equipe | Qualitativa | Avaliação (escala 1–5) do esforço cognitivo e técnico necessário para compreender e seguir a documentação de instalação. | ≤ 2 = Excelente (fácil) <br>3 = Moderado <br>≥ 4 = Difícil |
| **M13** | Compatibilidade entre navegadores | Quantitativa | Executar os mesmos fluxos principais (criar, reagendar, cancelar) em diferentes navegadores. <br>**Fórmula:** (Fluxos sem erro ÷ Total testados) × 100 | ≥ 95% = Excelente <br>80–94% = Boa <br><80% = Ruim |
| **M14** | Compatibilidade de execução em diferentes dispositivos | Quantitativa | Verificar se as funcionalidades principais permanecem utilizáveis e a interface se mantém legível em desktop, tablet e smartphone. <br>**Fórmula:** (Dispositivos com funcionamento completo ÷ Total de dispositivos testados) × 100 | 100% = Excelente <br>≥ 80% = Boa <br><80% = Insatisfatória |

---