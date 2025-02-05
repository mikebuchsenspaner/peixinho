# peixinho
<!DOCTYPE html>

<html  lang="en"> 

<head>

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Peixinho</title> 

    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
    </style>

    <script src="phaser.js"></script>

</head>


<body>

    <script src="peixe.js"></script> 
</body>
</html>
<script>
    document.title = "Mike";
</script>

<script>
    var resposta = "não, apesar disso acredito que tenha me virado bem";
    console.log(resposta);
</script>
</html>
var config = {
    type: Phaser.AUTO,
    width: 800,
    height: 600,
    scene: {
        preload: preload,
        create: create,
        update: update
    }
};

var game = new Phaser.Game(config);


var peixinho;

function preload() {
    this.load.image('mar', 'assets/bg_azul-claro.png');
    
    this.load.image('logo', 'assets/logo-inteli_branco.png');
   
    this.load.image('peixe', 'assets/peixes/baiacu.png');
    
    this.load.image('peixe2', 'assets/pepepepe.jpg');

}





function create() {
    this.add.image(400, 300, 'mar');

    this.add.image(400, 525, 'logo').setScale(0.50);

    this.add.image(400, 300, 'peixe2').setScale(0.80);

    peixinho = this.add.image(400, 300, 'peixe');
   
    peixinho.setFlip(true, false);
 }
function update() {                                                    

    peixinho.x = this.input.x;
    peixinho.y = this.input.y;

}

   
