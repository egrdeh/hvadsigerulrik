<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ulrik siger ikke nej, men tak for kage!</title>
</head>
<body>
    <!-- <h1>Ulrik siger ikke nej, men tak for kage!</h1> -->
    
<script>
        document.addEventListener('DOMContentLoaded', function() {
            var textElement = document.getElementById('text');
            var diceElement = document.getElementById('dice');
            var rollButton = document.getElementById('roll-button');
            var text1 = 'Ulrik siger ikke nej, men tak for kage!';
            var text2 = 'Ulrik siger er der mere slik?';
            var text3 = 'Skulle man mon k\u00F8be en ny motorcykel?';
            var diceFaces = ['&#9856;', '&#9857;', '&#9858;', '&#9859;', '&#9860;', '&#9861;'];

            function rollDice() {
                var roll = Math.floor(Math.random() * 6) + 1;
                diceElement.innerHTML = diceFaces[roll - 1];

                if (roll === 6) {
                    textElement.textContent = text2;
                    return;
                }

                if (Math.random() < 0.15) {
                    textElement.textContent = text3;
                    return;
                }

                textElement.textContent = text1;
            }

            rollButton.addEventListener('click', rollDice);
            rollDice();
        });
    </script>

<div id="text">Ulrik siger ikke nej, men tak for kage!</div>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }

        .dice-area {
            margin: 24px 0;
        }

        #dice {
            font-size: 96px;
            line-height: 1;
        }

        #roll-button {
            margin-top: 12px;
            padding: 10px 18px;
            font-size: 16px;
            cursor: pointer;
        }

        /* Style to resize the image */
        img {
            width: 40%; /* Set the width of the image to 40% of its original size */
            height: auto; /* Maintain aspect ratio */
        }
    </style>
    <div class="dice-area">
        <div id="dice">&#9856;</div>
        <button id="roll-button" type="button">Roll dice</button>
    </div>
    <!-- Image inserted from a URL -->
    <img src="https://hvadsigerulrik.dk/MicrosoftTeams-image.png" alt="Snitter">

</body>
</html>
