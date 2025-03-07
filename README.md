<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bạn có chơi Free Fire không?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: red;
            color: white;
        }
        img {
            width: 200px;
            height: auto;
            margin: 20px;
        }
        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        .btn {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div id="question">
        <h2>Bạn có chơi Free Fire không?</h2>
        <img src="https://thanhnien.mediacdn.vn/Uploaded/truongnghi/2022_06_21/1-5103.jpg" alt="Free Fire Logo">
        <div class="buttons">
            <button class="btn" id="yes">Có</button>
            <button class="btn" id="no">Không</button>
        </div>
    </div>
    
    <div id="result" class="hidden">
        <h1>Hahahaha Trẻ Trâu</h1>
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRsSqRQ3cFnSj7toe6TdqEfCP7qK6Nx20d9OA&s" alt="Troll Face">
    </div>

    <script>
        document.getElementById("no").addEventListener("click", function() {
            let yesBtn = document.getElementById("yes");
            let noBtn = document.getElementById("no");
            let currentSizeYes = parseFloat(window.getComputedStyle(yesBtn).fontSize);
            let currentSizeNo = parseFloat(window.getComputedStyle(noBtn).fontSize);
            yesBtn.style.fontSize = (currentSizeYes * 1.2) + "px";
            noBtn.style.fontSize = (currentSizeNo * 0.8) + "px";
            noBtn.disabled = true;
        });
        
        document.getElementById("yes").addEventListener("click", function() {
            document.getElementById("question").classList.add("hidden");
            document.getElementById("result").classList.remove("hidden");
        });
    </script>
</body>
</html>
