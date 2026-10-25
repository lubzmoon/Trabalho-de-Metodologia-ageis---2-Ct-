# Trabalho de Metodologias Ágeis — 2º Ano CT

**Alunos:** Ygor Gustavo Gonçalves Da Silva e Geovanna Luíza Duarte Costa  
**Turma:** 2º Ano CT  
**Professor:** Jason  
**Data:** 25/10/2026  

---

## O que é GitHub?

GitHub é uma plataforma online para hospedar projetos e colaborar neles. Pessoas e equipes podem guardar arquivos, acompanhar alterações e conversar sobre melhorias. É muito usado no desenvolvimento de software, mas também pode organizar documentos, materiais de estudo e outros arquivos.

O GitHub utiliza o Git, um sistema de controle de versão. Em termos simples, o Git registra mudanças ao longo do tempo. Assim, é possível consultar versões anteriores e entender o que foi alterado. O GitHub oferece uma interface e ferramentas de colaboração em torno desses repositórios.

### Conceitos importantes

* **Repositório (repository):** espaço de um projeto que reúne arquivos e histórico de alterações. Pode ser público ou privado.
* **Commit:** registro de uma alteração, acompanhado de uma mensagem que explica o que foi feito.
* **Branch (ramificação):** linha de trabalho separada, útil para experimentar mudanças sem alterar imediatamente a versão principal.
* **Pull request:** proposta para revisar e integrar mudanças de uma branch em outra. Permite discutir as alterações antes de incorporá-las.
* **README:** arquivo de apresentação do projeto. Normalmente explica seu objetivo e como utilizá-lo. O GitHub costuma exibi-lo na página inicial do repositório.

---

## A Ligação do GitHub com a Aula 2 da Semana 21: Pipeline de Feedback e Cultura DevOps

Na nossa disciplina, aprendemos sobre a **Cultura DevOps**, que busca unir quem desenvolve o sistema (Dev) e quem cuida da infraestrutura/operação (Ops) para entregar software com mais agilidade e qualidade[cite: 2].

O tema central da **Aula 2 (SISANO1C3B4S21A2)** é o **Pipeline de Feedback**[cite: 2]. Em termos simples, um pipeline de feedback é uma esteira automática que pega o código alterado, faz o *build* (compilação), executa os testes e devolve uma resposta rápida à equipe sobre o estado daquele código[cite: 7, 8].

### O Custo do Atraso e a Mentalidade *Fail Fast*
A regra de ouro que vimos na aula é: **quanto mais tempo demoramos para descobrir um erro, mais caro e complexo fica corrigi-lo**[cite: 9]. 
* Se um bug for descoberto em 2 minutos logo que o código é enviado, o aluno/desenvolvedor corrige-o na hora[cite: 6].
* Se o bug for para produção e ficar falhando durante o fim de semana, o prejuízo e o retrabalho são enormes[cite: 6].

Por isso usamos a mentalidade ***fail fast*** (falhar rápido)[cite: 7, 12]: queremos que o sistema aponte qualquer erro o mais cedo possível. Trabalhar em **pequenos lotes** (fazer alterações pequenas e frequentes em vez de um código gigante de uma só vez) ajuda a equipe a receber feedback quase instantâneo[cite: 9].

---

## Como os Recursos do GitHub Sustentam o Ciclo de Feedback

O GitHub não é só uma pasta na nuvem. Tem ferramentas que garantem tanto o **feedback humano** como o **feedback automatizado**[cite: 1, 2]:

### A. Issues (Feedback de Problemas e Ideias)
As **Issues** funcionam como um painel de recados e tarefas do projeto[cite: 8]. É onde qualquer membro da equipe ou usuário registra um bug encontrado, sugere uma melhoria ou detalha uma nova tarefa. O feedback começa aqui, mapeando a necessidade antes de o código ser escrito.

### B. Pull Requests (Feedback Humano e Revisão por Pares)
Quando vamos enviar uma alteração para o projeto principal, criamos um **Pull Request (PR)**. O PR é a etapa de feedback humano: os colegas de equipe analisam o código, fazem comentários, sugerem mudanças na lógica e só aprovam quando tudo estiver correto. Isso evita que códigos com erros entrem diretamente na versão principal.

### C. GitHub Actions (Feedback Automatizado — Integração Contínua)
O **GitHub Actions** é a ferramenta que constrói o pipeline de feedback propriamente dito[cite: 8]. Sempre que alguém faz um commit ou abre um Pull Request, o GitHub Actions dispara um *workflow* (esteira) automatizado que tenta executar o projeto e roda os testes criados pela equipe[cite: 7, 8]. 
* Se os testes passarem, mostra um ícone verde de sucesso (badge)[cite: 7, 8].
* Se algum teste falhar, avisa imediatamente na tela, impedindo que o código defeituoso avance[cite: 7, 12].

---

## Exemplo Prático: O Site de Horários da Turma

Para ficar bem claro como isso funciona na nossa rotina escolar do 2º CT, imagine que o nosso grupo está desenvolvendo um **site de horários das aulas**:

1. **Problema identificado (Issue):** Um colega avisa que a aula de quarta-feira está com o horário errado no site e abre uma **Issue** relatando o erro.
2. **Correção e Proposta (Pull Request):** O aluno responsável corrige a informação no seu código local e envia a mudança abrindo um **Pull Request**.
3. **Revisão da Equipe:** A dupla lê o código no PR, faz um comentário pedindo um ajuste de formatação e aprova.
4. **Verificação Automática (GitHub Actions):** O GitHub Actions executa automaticamente a esteira de testes e confirma que o layout não quebrou.
5. **Entrega e Novo Ciclo:** A alteração é aprovada e vai para o ar. Os colegas usam o site e, se notarem algo novo, abrem outra Issue, reiniciando o ciclo de melhoria contínua.

---

## Limites da Ferramenta e Considerações Finais

Apesar de o GitHub ser essencial, é importante entender os seus limites:

1. **Ferramenta não cria cultura sozinha:** Ter o GitHub configurado não significa ter Cultura DevOps. A cultura depende de comunicação, colaboração e compromisso da equipe.
2. **Testes aprovados não garantem 100% de perfeição:** Os testes automáticos só validam o que foram programados para testar. Um teste verde significa que o código passou nas regras criadas, mas não garante a ausência total de bugs não previstos.
3. **Necessidade de outras integrações:** Para monitorar o sistema rodando na nuvem em tempo real (como uso de memória ou erros de servidor), muitas vezes precisamos conectar o GitHub a ferramentas externas de monitoramento.

---

## Referências Consultadas

* **DORA.** *Working in small batches*. Disponível em: <https://dora.dev/capabilities/working-in-small-batches/>. Acesso em: 2026.
* **GITHUB DOCS.** *About issues*. Disponível em: <https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues>. Acesso em: 2026.
* **GITHUB DOCS.** *Continuous integration with GitHub Actions*. Disponível em: <https://docs.github.com/en/actions/get-started/continuous-integration>. Acesso em: 2026.
* **GITHUB DOCS.** *Reviewing proposed changes in a pull request*. Disponível em: <https://docs.github.com/en/pull-requests/how-tos/review-pull-requests/reviewing-proposed-changes-in-a-pull-request>. Acesso em: 2026.
* **MICROSOFT LEARN.** *Implement continuous feedback in DevOps*. Disponível em: <https://learn.microsoft.com/en-us/training/paths/az-400-implement-continuous-feedback/>. Acesso em: 2026.
* **SEDUC-SP.** *Desenvolvimento de Sistemas — 2º Ano CT: Cultura DevOps e feedback contínuo* (Código da Aula: SISANO1C3B4S21A2). São Paulo, 2026.
