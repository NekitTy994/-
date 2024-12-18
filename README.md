<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Машинка</title>
    <link rel="stylesheet" href="машинка.css">
</head>
<body>
    <div class="landscape">
        <div class="car"></div>
    </div>
</body>
</html>


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: #87CEEB; 
}

.landscape {
    position: relative;
    height: 200px;
    overflow: hidden;
}

.car {
    position: absolute;
    width: 200px;
    height: 100px;
    background-color: #FF5733;
    border-radius: 10px 10px 0 0;
    bottom: 20px;
    animation: drive 3s linear forwards;
}

.car::before,
.car::after {
    content: '';
    position: absolute;
    width: 40px;
    height: 40px;
    background-color: #333;
    border-radius: 50%;
}

.car::before {
    left: 20px;
    bottom: -20px;
}

.car::after {
    right: 20px;
    bottom: -20px;
}

@keyframes drive {
    from {
        left: -200px;
    }
    to {
        left: calc(100% - 250px);
    }
}

.landscape::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 20px;
    background-color: #555;
    bottom: 0;
}
