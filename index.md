<html>

<head>
    <title>
        mentalista 🔮
    </title>
</head>
<style>
    body {
        font-family: 'Roboto Mono',monospace;
        min-height: 600px;
        background-image: linear-gradient(to bottom,#100b57,#600c79);
        background-color: #000000;
        background-size: cover;
        background-position: center bottom;
        background-repeat: no-repeat;
    }

    .page-footer{
        color: #ffffffc2;
        font-family:'Courier New', Courier, monospace;
        position:absolute;
        bottom:0;
        width:0%
    }

    .container {
        text-align: center;
        padding: 20px;
        height: 100vh;
    }
  
    .page-title {
        color: #ffffff;
        margin: 0 0 5px;
    }
  
    .page-subtitle {
        color: #ffffff;
        margin-top: 5px;
    }
  
    .page-logo {
        width: 200px;
    }
  
    .alura-logo {
        width: 40px;
        position: absolute;
        top: 10px;
        right:10px;
    }
  
    @media (max-height: 500px) {
        body {
            min-height:800px;
        }
    }
    h2{
        color:#ff00008e;
        text-align: center;
    }
    span{
        background-color:#0d0852;
        color: #ffffff;
    }
</style>
<body>
    <div class="container">
        <h1 class="page-title">
            🔮 <br>Mentalista 
        </h1>
        <br>
        <br>
        <br>
        <p id= "resposta", class="page-subtitle">  
            o numero que você tinha que descobrir era: 
        </p>
    </div>
    <a href="https://alura.com.br/" target="_blank">
        <img src="https://www.alura.com.br/assets/img/home/alura-logo.svg" alt="" class="alura-logo">
    </a>
    <footer class="page-footer">Imersão<span>Dev_</span></footer>
</body>
<script>
    function aleatorio(min,max){
        min = Math.ceil(min)
        max = Math.floor(max)
        return Math.floor(Math.random() * (max-min)) + min
    }
    let chute = prompt('tente adivinhar qual numero entre 0 e 10 o computador escolheu')
    let secreto = aleatorio(1,10)
    console.log('ta indo')
    let i = 0
    do{
        if(secreto == chute){
            document.getElementById('resposta').innerHTML=`<p class="page-subtitle">o numero que você tinha que descobrir era: ${chute}</p>`
            i++
        }else{
            if(secreto > chute){
                chute = prompt('É MAIOR')
            }else{
                chute = prompt('É MENOR')    
            }
        }
    }while(i == 0)    
</script>
</html>
