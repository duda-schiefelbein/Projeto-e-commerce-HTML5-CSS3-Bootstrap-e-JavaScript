📜 Documentação da Lógica JavaScript (funcoes.js)
Esta documentação descreve o funcionamento de todas as funções implementadas no ficheiro JavaScript responsável pela interatividade e cálculo automático do carrinho de compras da loja virtual Eletro-tech.

🛠️ Descrição das Funções
1. alterarQtd(produto, acao)
Aumenta ou diminui a quantidade de um produto selecionado e atualiza o seu valor total unitário na tabela.

Parâmetros:

produto (String / Number): Identificador do produto (ex: 1, 2, 3).

acao (String): Ação a ser executada ('+' para incrementar ou '-' para decrementar).

Comportamento:

Valida se a quantidade atual é 0 ao tentar subtrair. Se for, exibe um alerta de aviso e impede valores negativos.

Atualiza o contador de quantidade no elemento qtd_{produto}.

Recalcula o subtotal do item multiplicando a quantidade pelo valor unitário limpo.

Atualiza o elemento total_{produto} formatado como moeda.

Chama a função soma() para recalcular o total geral da compra.

2. soma()
Calcula o valor total acumulado de todos os produtos do carrinho e atualiza o subtotal geral da página.

Parâmetros: Nenhum.

Comportamento:

Percorre iterativamente os totais dos produtos (do ID total_1 ao total_3).

Extrai os valores numéricos de cada item utilizando a função somenteNumeros().

Soma os valores numéricos e atualiza o elemento HTML subtotal formatado com formatarValor().

3. somenteNumeros(n)
Função utilitária de tratamento de dados que remove todos os carateres não numéricos de uma string de texto.

Parâmetros:

n (String): Texto contendo valor monetário ou carateres formatados (ex: "R$ 1.500,00").

Retorno:

(String): Apenas os dígitos numéricos encontrados na string (utilizando a expressão regular /\D/g).

4. formatarValor(n)
Função utilitária para formatação monetária no padrão brasileiro (Real - BRL).

Parâmetros:

n (Number / String): O valor numérico a ser formatado.

Retorno:

(String): String formatada com o prefixo "R$" e separadores regionais adequados (ex: R$1500).

📌 Requisitos de Integração no HTML
Para que as funções operem corretamente no DOM, o ficheiro HTML deve conter os seguintes elementos com convenção de ID correspondente:

Quantidade: id="qtd_1", id="qtd_2", id="qtd_3"

Valor Unitário: id="valor_1", id="valor_2", id="valor_3"

Total do Item: id="total_1", id="total_2", id="total_3"

Subtotal Geral: id="subtotal"

🚀 Tecnologias Utilizadas
JavaScript (ES6+)

DOM Manipulation (Document Object Model)

Regex (Expressões Regulares)
