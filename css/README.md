🛒 Eletro-Tech-Store (Lojinha)

Este é um projeto simples de carrinho de compras de uma loja de eletrônicos, desenvolvido com HTML5, CSS3, Bootstrap e JavaScript.

📁 Estrutura do Projeto

A estrutura de diretórios e arquivos do projeto está organizada da seguinte forma:

/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── funcoes.js
└── img/
    ├── produto_1.jpg
    ├── produto_2.jpg
    └── produto_3.jpg


📄 Código HTML Original (index.html)

Abaixo está o código HTML original do projeto:

<!DOCTYPE html>
<html>
<head>
    <title> Lojinha</title>
    <meta charset="UTF-8">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.13.1/font/bootstrap-icons.min.css">
<link rel="stylesheet" href="css/style.css">

<script src="js/funcoes.js"></script>

</head>
<body>
  <div class="container">

    <h1> <i id="icone-carrinho" class="bi bi-cart-check"></i> Eletro-Tech-Store </h1>
    <table class="table table-hover">
        <thead>
            <tr>
                <th> Imagem </th>
                <th> Produto</th>
                <th> Preço Unitário </th>
                <th> Qtd </th>
                <th> Total </th>
            </tr>
            </thead>
            <tbody>
                 <tr>
              <td>
                <img src="img/produto_1.jpg" alt="produto_1" width="100">
              </td>  
              <td> <div>Celular </div>
                <div><span class="produto-item">Código:</span> 4400 </div>
                <div><span class="produto-item"> Cor:</span> Laranja</div>
             </td> 
              <td id="valor_1"> R$ 8.000</td> 
              <td> <span class="badge text-bg-danger" onclick="alterarQtd(1,'-')"><i class="bi bi-dash"></i></span>
               <span id="qtd_1">0</span> 
                  <span class="badge text-bg-success" onclick="alterarQtd(1,'+')"><i class="bi bi-plus"></i></span></td> 
              <td id="total_1"> 0</td> 
              </tr>
              <tr>

              <td>
                <img src="img/produto_2.jpg" alt="produto_2" width="140">
              </td>  
              <td> <div>Notebook </div>
                <div><span class="produto-item"> Código:</span>3800 </div>
                <div><span class="produto-item" >Cor:</span> Preto</div>
             </td> 
              <td id="valor_2"> R$3.000</td> 
              <td> <span class="badge text-bg-danger" onclick="alterarQtd(2,'-')"><i class="bi bi-dash"></i></span>
                <span id="qtd_2">0</span> 
                <span class="badge text-bg-success" onclick="alterarQtd(2,'+')"><i class="bi bi-plus"></i></span></td> 
              <td id="total_2"> 0</td> 
              </tr>

               <td>
                <img src="img/produto_3.jpg" alt="produto_3" width="140">

              </td>  
              <td> <div> Televisor </div>
                <div> <span class="produto-item"> Código:</span> 1800 </div>
                <div> <span class="produto-item">Cor:</span> Preto </div>
             </td> 
              <td id="valor_3"> R$2.800</td> 
              <td> <span class="badge text-bg-danger" onclick="alterarQtd(3,'-')"><i class="bi bi-dash"></i></span>
                <span id="qtd_3">0</span> 
                 <span class="badge text-bg-success" onclick="alterarQtd(3,'+')"><i class="bi bi-plus"></i></span></td> 
              <td id="total_3"> 0</td> 
              </tr>

            </tbody>
        </thead>
    </table>
<footer class="text-center">
    <span><i class="bi bi-currency-dollar"></i> Subtotal:<span id="subtotal"> R$ 0 </span> </span>
</footer>
</div>
</body>

</html>


🎨 Estilização e CSS (css/style.css)

O projeto faz uso de duas fontes principais de CSS:

Bootstrap 5 (CDN): Utilizado para a estrutura responsiva (container), tabelas estilizadas (table, table-hover), distintivos/botões (badge, text-bg-danger, text-bg-success) e alinhamentos textuais (text-center).

Bootstrap Icons (CDN): Utilizado para a inclusão de ícones no carrinho (bi-cart-check), botões de incremento/decremento (bi-dash, bi-plus) e cifrão (bi-currency-dollar).

CSS Customizado (css/style.css): Arquivo responsável por aplicar personalizações pontuais ao layout.

Sugestão de CSS Personalizado (css/style.css)

Com base nos seletores e IDs definidos no seu HTML original, aqui está uma sugestão para o seu arquivo css/style.css:

/* Estilização do cabeçalho e ícone do carrinho */
h1 {
    margin-top: 20px;
    margin-bottom: 20px;
}

#icone-carrinho {
    color: #0d6efd;
    margin-right: 8px;
}

/* Estilização dos rótulos dos detalhes do produto */
.produto-item {
    font-weight: bold;
    color: #6c757d;
}

/* Ajustes nos botões de quantidade */
.badge {
    cursor: pointer;
    user-select: none;
}

/* Estilização do rodapé / subtotal */
footer {
    margin-top: 30px;
    font-size: 1.25rem;
    font-weight: bold;
}


⚙️ Funcionalidades Esperadas (js/funcoes.js)

Para que as interações do HTML funcionem corretamente, o arquivo js/funcoes.js deve implementar a função alterarQtd(id, operacao) chamada nos eventos onclick das badges de soma (+) e subtração (-).
