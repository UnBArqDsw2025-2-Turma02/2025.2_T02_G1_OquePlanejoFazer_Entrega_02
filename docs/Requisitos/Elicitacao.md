# Elicitação de Requisitos
## Introdução
A elicitação de requisitos é a etapa do desenvolvimento de software em que buscamos entender o que o sistema precisa ter e fazer para atender às necessidades dos usuários. Nessa fase, o objetivo é levantar informações de diferentes formas, para transformar as necessidades em requisitos claros e bem definidos.

## Metodologia
Para levantar os requisitos deste projeto, utilizamos duas técnicas principais: **benchmarking** e **brainstorming**.

* No benchmarking, analisamos sites e aplicativos já existentes no mercado com propostas semelhantes, para identificar funcionalidades, boas práticas e pontos de melhoria que poderiam ser aproveitados no nosso sistema.
* No brainstorming, aproveitamos o conhecimento adquirido no benchmarking e nossas próprias ideias para elaborar uma versão inicial dos requisitos.


Os principais sites analisados foram:

* [Todoist](https://www.todoist.com/pt-BR)
* [Tweek](https://tweek.so/pt-br)
* [Google Agenda](https://calendar.google.com/calendar)
* [Any.do](https://www.any.do/)

Essa combinação de técnicas permitiu unir a nossa visão com referências de soluções consolidadas no mercado, resultando em um conjunto de requisitos coerentes.

## Resultados
### Benchmarking
Ao analisarmos os sites selecionados, identificamos algumas funcionalidades recorrentes, como:
* Criação e gestão de tarefas com possibilidade de definir datas de vencimento e níveis de prioridade (Todoist, Any.do, Google Agenda).
* Organização em listas ou projetos, permitindo separar áreas da vida ou do trabalho (Todoist, Any.do, Tweek).
* Integração com calendário para visualizar compromissos e tarefas em uma mesma agenda (Google Agenda, Any.do).
* Visualizações variadas, como lista, calendário semanal (Tweek, Google Agenda) ou quadros no estilo Kanban (Any.do).
* Recorrência de tarefas e lembretes, facilitando o acompanhamento de rotinas (Todoist, Any.do, Google Agenda).
* Colaboração e compartilhamento, permitindo dividir listas e atribuir tarefas a outras pessoas (Todoist, Any.do).

Percebemos que, de modo geral, os sites analisados mantêm o foco na tarefa e em seus principais atributos, que em grande parte são semelhantes entre as plataformas. Dessa forma, entendemos que não precisamos de muitas funcionalidades, mas sim garantir o essencial, oferecendo ao usuário uma experiência simples e fluída.

## Brainstorming
Com base no que aprendemos na etapa de benchmarking, elaboramos no Miro uma versão inicial dos requisitos do sistema. Essa representação visual nos ajudou a organizar as ideias, relacionar funcionalidades e estruturar um ponto de partida para posteriormente formalizar esses requisitos.

<iframe width="768" height="496" src="https://miro.com/app/live-embed/uXjVJKT6240=/?focusWidget=3458764639921353795&embedMode=view_only_without_ui&embedId=540081705361" frameborder="0" scrolling="no" allow="fullscreen; clipboard-read; clipboard-write" allowfullscreen></iframe>



### Lista de Requisitos - Não formalizados

| Requisitos                                           | Critérios de Aceitação                                                                                |
| ---------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Login                                                | Integrar com Google.                                          |
| Cadastro                                             | Deve ser possível cadastrar-se com e-mail, usuário e senha.                                   |
| Criar tarefa/to-do                                   | Deve haver um campo "Título" obrigatório para salvar a tarefa. <br> Deve ser possível anexar múltiplos conteúdos à tarefa, como arquivos (PDFs, imagens) e links., <br>  O usuário deve poder definir uma data de prazo para a conclusão da tarefa. <br> Deve haver um campo de "Descrição" para adicionar mais detalhes, sendo seu preenchimento opcional. <br> Deve ser possível escolher e associar uma ou mais "Tags" à tarefa. <br> O usuário deve poder escolher uma cor específica dentro de um grupo pré definido para a identificação visual da tarefa. <br> Deve ser possível definir um nível de Prioridade para a tarefa (ex: Alta, Média, Baixa).                                          |
| Editar tarefa                                        | Pode editar todos os campos inseridos na criação da tarefa. <br> Flag de obrigatório. <br> color coding das tarefas. <br> Adicionar estrela de tarefa favorita. <br> Permitir que o usuário clique na tarefa e priorize ela.                     |
| Priorizar tarefas                                    | Deve ser possível clicar na tarefa e atribuir prioridade (Alta, Média, Baixa).                        |
| Visualizar tarefa                                    | Visualizar em matriz de eisenhower. <br>  Exibição de Grafíco de Gantt. |
| Excluir tarefa                                       | Permitir que o usuário clique na tarefa e priorize ela                                         |
| Finalizar tarefa                                     |                                  |
| Criar lista/categorias                               | Criar tags para categorizar tarefas (trabalho, saúde, etc)                                  |
| Visualização do calendário (diário, semanal, mensal) | Deve ser possível aplicar filtro na visualização.                              |
| Permitir sync com o Agendas          | O sistema deve sincronizar automaticamente com agendas externas.                                      |
| Relatório e progresso                 | O sistema deve gerar um resumo de atividades realizadas ou mão. <br> Incluir gráficos.                                 |
| Alertas periódicos                                   | O sitema deve gerar alertas periodicos durante o dia para tarefas a serem realizadas.                                  |

---

### Lista de Requisitos Não Funcionais - Não formalizados

| Requisitos                                           | Critérios de Aceitação                                                                       |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| Criptografia de senhas                               | Deve ser utilizado em formato JWT. <br>  Deve ser armazenado no banco de dados.                             |
| Compatibilidade com diferentes sistemas | A gestão de sessão do usuário (login, logout, tokens) deve funcionar de forma idêntica e segura em todas as plataformas alvo. <br> Deve ser compatível com as versões 15 e 16 do Android. <br> Deve ser compatível com as versões 18 e 26 do IOS.                            |
| Interface responsiva                                 | Todo o conteúdo e funcionalidades devem estar presentes em todas as versões (desktop, tablet e mobile). <br> As imagens devem escalar proporcionalmente para caber em seus contêineres, sem distorção ou vazamento. <br> O tamanho da fonte deve garantir uma leitura confortável em qualquer dispositivo, sem necessidade de zoom. <br> O menu de navegação deve se transformar em um formato compacto em telas menores.           |
| Modo escuro                                          | Deve ser utilizado cores dessaturadas na paleta de cores escuras. <br> Deve permitir que os usuários ativem e desativem o modo escuro. <br> A taxa de contraste de cores não deve ser inferior a 4,5:1 para texto de tamanho normal.                                      |
| Feedback ao Usuário                         | O indicador visual de carregamento (ex: ícone giratório) deve ter uma alternativa textual para usuários que não podem percebê-lo visualmente. <br> O contraste entre o indicador de carregamento (e seu texto associado) e o fundo deve ser suficiente para ser claramente visível. <br> A cor não deve ser o único meio de transmitir o sucesso da operação. <br> O feedback deve ser apresentado de forma que tecnologias assistivas (como leitores de tela) possam detectá-lo e anunciá-lo ao usuário sem que ele precise procurar ativamente pela informação.                 |
| Conformidade com a LGPD                        | Os dados coletados devem ser classificados em categorias. <br> Deve ser identificado por que cada categoria de dados está sendo coletada. <br> Explicar, de forma transparente e detalhada, por que os dados dos usuários estão sendo coletados e como serão usados.                   |




<br>
Observação: Os requisitos apresentados nas duas tabelas acima estão intencionalmente fora do padrão formal de documentação, pois refletem o resultado de uma sessão de brainstorming, permitindo uma escrita mais livre e espontânea das ideias.




## Histórico de Versões

| Versão | Alteração | Responsável                              | Data     | Revisor                                  | Detalhes da Revisão | Data da Revisão |
| ------ | --------- | ---------------------------------------- | -------- | ---------------------------------------- | ------------------- | --------------- |
| 1.0    |  Elicitação de Requisitos    | [Yasmim Rosa](https://github.com/yaskisoba), [Millena Queiroz](https://github.com/MillenaQueiroz) e [Maria Clara](https://github.com/alvezclari) | 21/09/2025 | [Yasmim Rosa](https://github.com/yaskisoba) | ---- | xx/xx/xxxx |

