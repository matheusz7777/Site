<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Minha Loja</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f5f5;
    }

    header {
      background: #111;
      color: #fff;
      padding: 15px;
      display: flex;
      justify-content: space-between;
    }

    .logo {
      font-size: 20px;
      font-weight: bold;
    }

    .banner {
      background: linear-gradient(to right, #000, #444);
      color: #fff;
      padding: 60px 20px;
      text-align: center;
    }

    .produtos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      padding: 20px;
    }

    .produto {
      background: #fff;
      padding: 15px;
      border-radius: 10px;
      text-align: center;
    }

    .produto img {
      max-width: 100%;
    }

    button {
      background: #000;
      color: #fff;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }

    button:hover {
      background: #444;
    }

    #carrinho {
      position: fixed;
      right: 10px;
      bottom: 10px;
      background: #000;
      color: #fff;
      padding: 15px;
      border-radius: 10px;
    }
  </style>
</head>
<body>

<header>
  <div class="logo">Minha Loja</div>
  <div>Carrinho: <span id="total">0</span></div>
</header>

<section class="banner">
  <h1>Promoções Imperdíveis</h1>
  <p>Compre agora com os melhores preços</p>
</section>

<section class="produtos">
  <div class="produto">
    <img src="https://via.placeholder.com/200">
    <h3>Produto 1</h3>
    <p>R$ 99,90</p>
    <button onclick="adicionar(99.9)">Comprar</button>
  </div>

  <div class="produto">
    <img src="https://via.placeholder.com/200">
    <h3>Produto 2</h3>
    <p>R$ 149,90</p>
    <button onclick="adicionar(149.9)">Comprar</button>
  </div>
</section>

<div id="carrinho">
  Total: R$ <span id="valor">0.00</span>
</div>

<script>
  let total = 0;

  function adicionar(valor) {
    total += valor;
    document.getElementById("valor").innerText = total.toFixed(2);
    document.getElementById("total").innerText++;
  }
</script>

</body>
</html>
