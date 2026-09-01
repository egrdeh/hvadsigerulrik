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
            var orangeSceneElement = document.getElementById('orange-scene');
            var text1 = 'Ulrik siger ikke nej, men tak for kage!';
            var text2 = 'Ulrik siger er der mere slik?';
            var text3 = 'Skulle man mon k\u00F8be en ny motorcykel?';
            var text4 = 'Andreas spiser æbler og piller appelsiner forkert';
            var text5 = 'Er du ikke en del af kageordningen?';
            var diceFaces = ['&#9856;', '&#9857;', '&#9858;', '&#9859;', '&#9860;', '&#9861;'];

            function showOrangeScene(show) {
                orangeSceneElement.hidden = !show;
            }

            function rollDice() {
                var roll = Math.floor(Math.random() * 6) + 1;
                diceElement.innerHTML = diceFaces[roll - 1];
                showOrangeScene(false);

                if (roll === 3) {
                    textElement.textContent = text4;
                    showOrangeScene(true);
                    return;
                }

                if (roll === 6) {
                    textElement.textContent = text2;
                    return;
                }

                var specialRoll = Math.random();
                if (specialRoll < 0.10) {
                    textElement.textContent = text5;
                    return;
                }

                if (specialRoll < 0.25) {
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

        #text {
            font-size: 28px;
            margin-top: 24px;
        }

        #orange-scene {
            margin: 18px auto 10px;
            max-width: 360px;
        }

        #orange-scene img {
            width: min(100%, 320px);
            height: auto;
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
        body > img {
            width: 40%; /* Set the width of the image to 40% of its original size */
            height: auto; /* Maintain aspect ratio */
        }
    </style>
    <div id="orange-scene" hidden>
        <img src="orange-unwrapping.svg" alt="Stick figure unwrapping an orange">
    </div>
    <div class="dice-area">
        <div id="dice">&#9856;</div>
        <button id="roll-button" type="button">Roll dice</button>
    </div>
    <!-- Image inserted from a URL -->
    <img src="https://hvadsigerulrik.dk/MicrosoftTeams-image.png" alt="Snitter">

</body>
</html>
