<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
            font-family: 'Poppins', sans-serif;
            flex-direction: column;
            text-align: center;
        }

        h1 {
            color: #ffffff;
            font-family: 'Pacifico', cursive;
            font-size: 36px;
            margin-bottom: 40px;
        }

        .buttons {
            display: flex;
            gap: 40px; /* Mai multă distanță între butoane */
        }

        button {
            padding: 20px 50px;
            font-size: 24px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        #yes {
            background-color: #4CAF50;
            color: white;
        }

        #no {
            background-color: #f06292;
            color: white;
        }

        #yes:hover, #no:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <h1>Vrei să fii partenera mea de V-day? 💖</h1>
    <div class="buttons">
        <button id="yes">Yes</button>
        <button id="no">No</button>
    </div>

    <script>
        const yesButton = document.getElementById('yes');
        const noButton = document.getElementById('no');
        let scale = 1; // Inițializarea scale-ului pentru creștere incrementală

        noButton.addEventListener('mouseover', () => {
            noButton.style.transform = 'scale(0.8)';
            yesButton.style.transform = 'scale(1.5)';
        });

        noButton.addEventListener('click', () => {
            scale += 0.2; // Creștere treptată la fiecare click
            yesButton.style.transform = `scale(${scale})`;
            yesButton.style.backgroundColor = '#4CAF50';
        });

        yesButton.addEventListener('click', () => {
            // Redirecționează către o altă pagină
            window.location.href = "vdays2.html"; // Înlocuiește cu URL-ul dorit
        });
    </script>
</body>
</html>
