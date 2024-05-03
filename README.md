<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ulrik siger ikke nej, men tak for kage!</title>
</head>
<body>
    <!-- <h1>Ulrik siger ikke nej, men tak for kage!</h1> -->
    
<script>
        // JavaScript code to alternate between two text strings every 10th visit
        document.addEventListener('DOMContentLoaded', function() {
            var textElement = document.getElementById('text');
            var text1 = 'Ulrik siger ikke nej, men tak for kage!';
            var text2 = 'Ulrik siger er der mere slik?';
            var visitCount = parseInt(localStorage.getItem('visitCount')) || 0;

            // Increment visit count and save to localStorage
            visitCount++;
            localStorage.setItem('visitCount', visitCount);

            // Determine if it's the 10th visit
            if (visitCount % 10 === 0) {
                textElement.textContent = text2; // Display text2 on the 10th visit
            } else {
                textElement.textContent = text1; // Display text1 on other visits
            }
        });
    </script>

<div id="text">Ulrik siger ikke nej, men tak for kage!</div>
<head>
        <style>
        /* Style to resize the image */
        img {
            width: 40%; /* Set the width of the image to 40% of its original size */
            height: auto; /* Maintain aspect ratio */
        }
    </style>
</head>
    <!-- Image inserted from a URL -->
    <img src="https://hvadsigerulrik.dk/MicrosoftTeams-image.png" alt="Snitter">

</body>
</html>
