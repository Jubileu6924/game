
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400..900&display=swap" rel="stylesheet">
    <title>Em busca da cidade perdida</title>
</head>
<body>
    <main>
        <div class="passo ativo" id="passo-0">
            <p>um dia desse, dentro de um livro da biblioteca da escola, descobri uma carta antiga sobre uma cidade perdida, escondidas por riquezas e belezas naturais. Nesta carta, a autora deixa algumas pistas para encontrar essa cidade perdida e eu decide segui-las!</p>
            <button class="btn-proximo" data-proximo="1">Rio de janeiro </button>
            <button class="btn-proximo" data-proximo="2">Pernambuco </button>
        </div>
        <div class="passo" id="passo-0">
            <p>Você vai começa a sua jornada no Rio de janeiro subindo o pico da Tijuca ao amanhecer para encontrar a primeira pista.</p>
            <button class="btn-proximo" data-proximo="3">Procura a pista no topo do pico </button>
            <button class="btn-proximo" data-proximo="4">Desistir e voltar para casa </button>
        </div>
    </main>
    <script src="script.js"></script>
    
</body>
</html>

java script:
const avanca = document.querySelectorAll('.btn-proximo');

avanca.forEach(button => {
    button.addEventLister('click', function(){
        const atual = document.querySelector('.ativo');
        const proximoPasso = 'passo-' + this.getAttribute('data-proximo'); 
    
        atual.classList.remove('ativo');
        DocumentFragment.getElementByld(proximoPasso).classList.add('ativo');
    })
})

css:
body{
    background-color:rgb(44, 0, 75);
    color: white;
    font-family: "Cinzel", serif;
    display: flex;
    justify-content:center;
    align-items: center;
    height: 700px;
    margin: 0;
}

button {
    background-color:rgb(24, 0, 245);
    color: white;
    font-family: "Cinzel", serif;
}







