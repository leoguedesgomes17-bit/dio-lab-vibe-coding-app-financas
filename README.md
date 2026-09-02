## Imagens do projeto

### Dashboard

![Dashboard do Tranquil Money Manager](dashboard-final.jpg)

### Carteiras

![Página de carteiras](carteiras.jpg)

### Cadastro de transação

![Cadastro de nova transação](cadastro-transacao.jpg)

### Gráfico de despesas

![Gráfico de despesas por categoria](grafico-despesas.jpg)
## Funcionalidades

- Dashboard com saldo atual, total de receitas e total de despesas;
- Cadastro de receitas e despesas;
- Cadastro e edição do valor do salário mensal;
- Criação e gerenciamento de carteiras manuais;
- Transferências entre carteiras sem alterar o patrimônio total;
- Agente Financeiro com interação em linguagem natural;
- Registro e classificação de movimentações por conversa;
- Categorias como alimentação, moradia, transporte, saúde, lazer, educação e salário;
- Histórico de movimentações;
- Filtros por tipo, categoria e período;
- Gráfico de despesas por categoria;
- Relatórios de receitas, despesas e evolução patrimonial;
- Edição e exclusão de lançamentos;
- Mensagens de confirmação e validação dos formulários;
- Interface responsiva para computador e celular;
- Dados de demonstração para facilitar a apresentação do projeto.

## Prompt final — PRD

O texto abaixo foi utilizado como prompt principal para orientar a criação do aplicativo no Lovable.

```text
Crie um aplicativo web completo e responsivo de finanças pessoais chamado “Tranquil Money Manager”.

1. OBJETIVO

O Tranquil Money Manager deve ajudar o usuário a organizar a vida financeira de maneira simples. Ele deverá permitir o controle de salário, receitas, despesas e diferentes carteiras, além de apresentar saldo, patrimônio total, gráficos e histórico de movimentações.

O aplicativo será um projeto educacional. Não solicite senhas bancárias, números completos de cartões, tokens ou outros dados financeiros sensíveis. Nesta versão, as carteiras serão cadastradas manualmente e não terão conexão real com bancos.

2. PÚBLICO-ALVO

Jovens e adultos que desejam controlar o orçamento pessoal sem utilizar planilhas ou sistemas financeiros complexos.

3. IDIOMA E FORMATAÇÃO

- Utilize português do Brasil em toda a interface.
- Exiba valores no formato monetário brasileiro, como “R$ 1.250,00”.
- Exiba datas no formato “DD/MM/AAAA”.
- Utilize textos claros, amigáveis e fáceis de compreender.

4. IDENTIDADE VISUAL

- Crie uma interface moderna, limpa, amigável e profissional.
- Utilize azul ou roxo como cor principal da marca.
- Utilize verde para receitas e valores positivos.
- Utilize vermelho ou coral para despesas e valores negativos.
- Use fundo claro, cartões com cantos arredondados, sombras suaves e ícones consistentes.
- Garanta boa legibilidade e contraste.
- Evite excesso de informações na mesma tela.
- Crie uma experiência responsiva para computador, tablet e celular.

5. NAVEGAÇÃO

Crie um menu com as páginas:

- Visão geral;
- Transações;
- Carteiras;
- Relatórios;
- Configurações.

No celular, transforme o menu em navegação inferior ou menu recolhível.

6. CABEÇALHO

- Exiba o nome e a identidade visual do Tranquil Money Manager.
- Mostre uma mensagem curta de boas-vindas.
- Inclua um botão de destaque chamado “Nova transação”.
- Inclua um botão para alternar entre tema claro e escuro, se isso não comprometer as funcionalidades principais.

7. DASHBOARD — VISÃO GERAL

Crie cartões de resumo para:

- Patrimônio total;
- Saldo disponível;
- Salário mensal;
- Total de receitas do mês;
- Total de despesas do mês;
- Economia do mês.

Regras dos indicadores:

- O patrimônio total deve ser a soma dos saldos de todas as carteiras.
- A economia do mês deve ser calculada como receitas menos despesas.
- Os cartões devem ser atualizados automaticamente após qualquer cadastro, edição, exclusão ou transferência.
- O cartão de salário deve conter o botão “Editar salário”.

Inclua também:

- Um gráfico de rosca com as despesas por categoria;
- Um gráfico de barras ou linhas comparando receitas e despesas dos últimos meses;
- Uma lista com as cinco movimentações mais recentes;
- Um resumo dos saldos das carteiras;
- Um filtro de período para os gráficos.

8. SALÁRIO MENSAL EDITÁVEL

- Durante o primeiro uso, permita informar o salário mensal.
- Exiba o salário em um cartão próprio no dashboard.
- Inclua o botão “Editar salário”.
- Ao clicar, abra um modal com o valor atual preenchido.
- Aceite apenas valores numéricos iguais ou maiores que zero.
- Após salvar, atualize imediatamente o salário, as receitas, o saldo e os indicadores relacionados.
- Exiba uma mensagem de sucesso.
- Trate o salário como uma receita mensal recorrente.
- Alterar o salário não deve criar lançamentos duplicados no mesmo mês.
- Permita selecionar em qual carteira o salário será recebido.
- Permita escolher o dia mensal de recebimento.

9. CARTEIRAS

Crie uma página chamada “Carteiras”. O usuário deve poder cadastrar manualmente diferentes locais onde guarda dinheiro, como:

- Conta principal;
- Conta digital;
- Carteira física;
- Poupança;
- Investimentos;
- Outros.

Para cada carteira, permita informar:

- Nome;
- Tipo;
- Saldo inicial;
- Cor;
- Ícone opcional.

Funcionalidades das carteiras:

- Criar, visualizar, editar e excluir carteiras;
- Mostrar cada carteira em um cartão com nome, tipo e saldo atual;
- Atualizar o saldo automaticamente após receitas, despesas e transferências;
- Permitir ocultar ou exibir os valores financeiros;
- Exibir o patrimônio total pela soma de todas as carteiras;
- Não permitir excluir uma carteira com movimentações sem antes exibir uma confirmação;
- Se a carteira possuir movimentações, permitir transferi-las para outra carteira antes da exclusão;
- Criar uma carteira inicial de demonstração chamada “Conta principal”.

10. TRANSFERÊNCIAS ENTRE CARTEIRAS

- Adicione a opção “Transferir”.
- Solicite carteira de origem, carteira de destino, valor, data e descrição opcional.
- Não permita selecionar a mesma carteira como origem e destino.
- Não permita valores iguais ou menores que zero.
- Avise quando o valor for superior ao saldo disponível, mas mantenha uma regra configurável para permitir ou impedir saldo negativo.
- Ao confirmar, diminua o saldo da carteira de origem e aumente o saldo da carteira de destino.
- A transferência não deve alterar o patrimônio total, nem ser contabilizada como receita ou despesa.
- Registre a transferência no histórico.
- Ao editar ou excluir uma transferência, recalcule corretamente os saldos envolvidos.

11. CADASTRO DE TRANSAÇÕES

Ao clicar em “Nova transação”, abra um modal ou formulário e permita selecionar:

- Receita;
- Despesa;
- Transferência.

Para receitas e despesas, solicite:

- Descrição;
- Valor;
- Categoria;
- Data;
- Carteira relacionada;
- Observação opcional;
- Opção para marcar como recorrente.

Categorias sugeridas:

- Alimentação;
- Moradia;
- Transporte;
- Saúde;
- Lazer;
- Educação;
- Compras;
- Assinaturas;
- Salário;
- Investimentos;
- Outros.

Regras:

- Todos os campos obrigatórios devem ser validados.
- Não aceite valor igual ou menor que zero.
- Depois de salvar, atualize o dashboard, os gráficos, o histórico e o saldo da carteira.
- Exiba uma mensagem confirmando o cadastro.
- Em despesas, diminua o saldo da carteira selecionada.
- Em receitas, aumente o saldo da carteira selecionada.
- Em transações recorrentes, permita selecionar frequência mensal e data de término opcional.

12. HISTÓRICO DE TRANSAÇÕES

- Liste receitas, despesas e transferências.
- Mostre descrição, categoria, carteira, data, tipo e valor.
- Diferencie visualmente cada tipo de movimentação.
- Permita pesquisar pela descrição.
- Permita filtrar por período, tipo, categoria e carteira.
- Permita ordenar por data e valor.
- Permita editar e excluir movimentações.
- Antes de excluir, solicite confirmação.
- Ao editar ou excluir, recalcule corretamente os cartões, gráficos e saldos das carteiras.
- Inclua paginação ou o botão “Carregar mais” caso existam muitas movimentações.

13. AGENTE FINANCEIRO COM IA

Crie uma área chamada “Assistente” com uma interface de conversa simples e acolhedora. O Agente Financeiro deve ajudar o usuário a compreender e organizar as próprias finanças, sem se apresentar como consultor financeiro profissional.

Funcionalidades esperadas:

- Permitir registrar receitas e despesas usando linguagem natural, por exemplo: “Gastei 45 reais no mercado hoje usando a Conta principal”.
- Interpretar descrição, valor, categoria, data, tipo e carteira a partir da mensagem.
- Antes de salvar, exibir um resumo da movimentação interpretada e solicitar confirmação do usuário.
- Se alguma informação obrigatória estiver ausente ou ambígua, fazer uma pergunta curta para completar o registro.
- Sugerir automaticamente uma categoria, permitindo que o usuário a altere antes de confirmar.
- Responder a perguntas simples com base nos dados do aplicativo, como “Quanto gastei com alimentação este mês?” ou “Qual foi minha maior categoria de despesas?”.
- Apresentar dicas educativas de economia com linguagem acessível, baseadas nos padrões de gastos exibidos no aplicativo.
- Ajudar o usuário a definir uma meta financeira simples e acompanhar seu progresso.
- Nunca prometer rendimentos, recomendar investimentos específicos ou substituir orientação profissional.
- Não inventar valores: quando não houver dados suficientes, informar isso claramente.
- Manter o cadastro manual por formulário como alternativa à conversa.

Se não houver integração real com um modelo de IA, crie uma simulação funcional e identifique claramente que se trata de um protótipo educacional. Não exponha chaves de API no código ou na interface.

14. METAS FINANCEIRAS

- Permita criar metas com nome, valor desejado, valor já economizado e prazo opcional.
- Mostre o progresso com barra e porcentagem.
- Permita editar, concluir e excluir metas.
- O Agente Financeiro pode sugerir um plano simples de economia, deixando claro que é uma estimativa educacional.

15. RELATÓRIOS

Crie uma página de relatórios contendo:

- Receitas e despesas por mês;
- Despesas por categoria;
- Evolução do patrimônio;
- Comparação entre meses;
- Carteiras com seus respectivos saldos;
- Filtro por período e carteira.

Se for possível, inclua um botão para exportar o histórico filtrado em CSV. Caso a exportação não seja implementada, não exiba um botão sem funcionamento.

16. CONFIGURAÇÕES

Permita configurar:

- Nome do usuário;
- Regra para permitir ou impedir saldo negativo;
- Tema claro ou escuro;
- Moeda padrão, mantendo real brasileiro como valor inicial;
- Preferência para exibir ou ocultar valores.

Inclua uma opção “Restaurar dados de demonstração”, com confirmação antes de substituir os dados atuais.

17. ESTADOS DA INTERFACE

- Crie estados vazios amigáveis quando não houver carteiras ou transações.
- Mostre indicadores de carregamento quando necessário.
- Exiba mensagens claras de sucesso e erro.
- Não permita envio duplicado ao clicar várias vezes no botão de salvar.
- Desabilite ações impossíveis e explique o motivo ao usuário.

18. DADOS DE DEMONSTRAÇÃO

Inclua dados fictícios para facilitar a apresentação:

- Usuário: Leonardo;
- Salário mensal: R$ 3.500,00;
- Carteira “Conta principal”;
- Carteira “Dinheiro”;
- Algumas receitas e despesas distribuídas entre categorias;
- Uma transferência entre as carteiras.
- Uma meta financeira fictícia;
- Exemplos de perguntas que podem ser enviadas ao Agente Financeiro.

Os dados devem ser claramente fictícios e podem ser editados ou excluídos.

19. ACESSIBILIDADE E RESPONSIVIDADE

- Garanta contraste adequado entre texto e fundo.
- Adicione rótulos aos campos dos formulários.
- Permita navegação por teclado.
- Mostre indicação visual de foco.
- Utilize textos alternativos ou nomes acessíveis nos ícones.
- Garanta áreas de toque adequadas em dispositivos móveis.
- Evite depender somente das cores para transmitir informações.

20. PRIVACIDADE E SEGURANÇA

- Não solicite credenciais bancárias ou informações financeiras sensíveis.
- Informe que as carteiras são manuais e não possuem integração bancária real.
- Não apresente uma conexão fictícia com Nubank, Mercado Pago ou qualquer banco.
- Inclua um aviso de que o aplicativo é educacional e não oferece aconselhamento financeiro.

21. REQUISITOS DE QUALIDADE

- Todos os botões visíveis devem funcionar.
- Não utilize links ou controles meramente decorativos.
- Mantenha os cálculos consistentes em toda a aplicação.
- Evite duplicação de salário, transferências e lançamentos recorrentes.
- Preserve os dados enquanto o usuário navega entre as páginas.
- Utilize componentes reutilizáveis e mantenha o visual consistente.
- Não altere funcionalidades que já estejam funcionando ao implementar novas melhorias.

22. CENÁRIOS OBRIGATÓRIOS PARA TESTE

Garanta que estes fluxos funcionem:

1. Criar uma carteira e informar o saldo inicial.
2. Editar o valor do salário e selecionar a carteira de recebimento.
3. Cadastrar uma receita e confirmar o aumento do saldo.
4. Cadastrar uma despesa e confirmar a redução do saldo.
5. Transferir dinheiro entre duas carteiras sem alterar o patrimônio total.
6. Editar e excluir uma transação, recalculando todos os valores.
7. Filtrar o histórico por carteira e categoria.
8. Visualizar o aplicativo em computador e celular.
9. Registrar uma despesa por linguagem natural, revisar os dados interpretados e confirmar o lançamento.
10. Fazer uma pergunta ao Agente Financeiro sobre os gastos do mês.

RESULTADO ESPERADO

Entregue um protótipo funcional, responsivo e visualmente consistente. O usuário deve conseguir controlar salário, receitas, despesas, transferências e carteiras manuais. Os saldos, cartões, gráficos e relatórios devem ser recalculados automaticamente após cada alteração. Priorize primeiro o funcionamento correto dos fluxos essenciais e depois os recursos visuais complementares.
```

## Processo de criação com IA

O projeto foi construído por meio de conversas iterativas com a inteligência artificial. Primeiro, descrevi o objetivo e as funcionalidades principais. Depois, analisei o resultado, testei os fluxos e solicitei ajustes mais específicos.

### Interação 1 — Criação inicial

Inclua aqui um print mostrando o envio do prompt principal ao Lovable.

![Prompt inicial enviado ao Lovable](docs/images/interacao-01.png)

### Interação 2 — Testes e melhorias

Inclua aqui um print de uma solicitação de melhoria, como um ajuste no formulário, no gráfico ou na versão para celular.

![Solicitação de melhoria](docs/images/interacao-02.png)

### Resultado final

Inclua aqui um print da tela principal do aplicativo pronto.

![Dashboard final do Tranquil Money Manager](docs/images/dashboard-final.png)

## Reflexão sobre o processo

### O que funcionou bem?

O prompt estruturado funcionou bem porque apresentou o objetivo, o público-alvo, as funcionalidades e o estilo visual esperado. Também foi útil dividir a aplicação em áreas menores, como dashboard, formulário e histórico. Isso tornou as solicitações mais claras e facilitou a avaliação de cada resultado entregue pela IA.

### O que não funcionou como o esperado?

Solicitações muito abertas nem sempre produziram o resultado que eu imaginava. Alguns detalhes visuais e comportamentos precisaram ser explicados novamente de forma mais específica. Também percebi que uma interface aparentemente pronta ainda precisava ser testada, pois determinados botões, filtros ou validações poderiam não funcionar corretamente na primeira versão.

### O que aprendi sobre conversar com IAs?

Aprendi que conversar com uma IA é um processo de colaboração e refinamento. Quanto mais contexto e critérios claros eu forneço, mais próximo o resultado fica da minha intenção. Também aprendi a testar o que foi criado, explicar exatamente o que precisa mudar e fazer pedidos menores e objetivos. O primeiro prompt não precisa produzir uma solução perfeita; ele serve como ponto de partida para sucessivas melhorias.

## Demonstração

- **Aplicativo publicado:** [Acessar o Tranquil Money Manager](https://tranquil-money-manager.lovable.app)
- **Repositório no GitHub:** [Ver projeto no GitHub](https://github.com/leoguedesgomes17-bit/dio-lab-vibe-coding-app-financas)

## Como executar os testes da apresentação

1. Abra o aplicativo publicado.
2. Confira o saldo, as receitas e as despesas do dashboard.
3. Cadastre uma nova despesa.
4. Clique em “Editar salário”, informe um novo valor e salve.
5. Verifique se o salário, o saldo e o total de receitas foram atualizados sem criar lançamentos duplicados.
6. Confira se os totais e o gráfico foram atualizados.
7. Utilize os filtros do histórico.
8. Edite uma transação.
9. Exclua uma transação e confira a mensagem de confirmação.
10. Abra o aplicativo no celular ou reduza a janela para verificar a responsividade.

## Ferramentas utilizadas

- Lovable;
- Inteligência artificial generativa;
- GitHub;
- Vibe Coding.

## Autor

Desenvolvido por Leonardo Guedes Gomes como parte do desafio da **DIO**.

## Aviso

Este projeto tem finalidade educacional. Os dados exibidos são fictícios e o aplicativo não oferece aconselhamento financeiro.
