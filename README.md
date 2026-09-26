<!DOCTYPE html>
<html>
<head>
    <title>My Proposal 💗</title>

    <style>
        body {
            margin: 0;
            background: #fff0f5;
            font-family: Arial, sans-serif;
            text-align: center;
        }

        /* BOTH PAGES */
        .page {
            min-height: 100vh;
            display: none;
            justify-content: center;
            align-items: center;
        }

        .page.active {
            display: flex;
        }

        .box {
            background: white;
            width: 80%;
            max-width: 400px;
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 5px 25px #ffb6c1;
        }

        /* HEART */
        .heart {
            font-size: 80px;
            animation: beat 1s infinite;
        }

        @keyframes beat {
            0% {
                transform: scale(1);
            }

            50% {
                transform: scale(1.2);
            }

            100% {
                transform: scale(1);
            }
        }

        h1 {
            color: #ff4f81;
            font-size: 32px;
        }

        p {
            color: #555;
            font-size: 19px;
            line-height: 1.5;
        }

        /* BUTTON */
        button {
            padding: 13px 30px;
            margin: 10px;
            border-radius: 10px;
            font-size: 17px;
            cursor: pointer;
        }

        .yes {
            background: #ff4f81;
            color: white;
            border: none;
        }

        .no {
            background: white;
            color: #ff4f81;
            border: 2px solid #ff4f81;
        }

        button:hover {
            transform: scale(1.1);
        }

        /* PAGE 2 */
        .big-heart {
            font-size: 100px;
        }

        .message {
            color: #ff4f81;
            font-size: 24px;
            font-weight: bold;
        }

        .back {
            background: #ff4f81;
            color: white;
            border: none;
        }
    </style>
</head>

<body>

    <!-- PAGE 1 -->
    <div id="page1" class="page active">

        <div class="box">

            <div class="heart">❤️</div>

            <h1>My Proposal 💌</h1>

            <p>
                Naa ko iingon ba...
            </p>

            <p>
                sorry napo please babe🥺
            </p>

            <button class="yes" onclick="goToPage2()">
                YES ❤️
            </button>

            <button class="no" onclick="sayNo()">
                NO
            </button>

            <p id="noMessage"></p>

        </div>

    </div>


    <!-- PAGE 2 -->
    <div id="page2" class="page">

        <div class="box">

            <div class="big-heart">💗</div>

            <h1>Yay! ❤️</h1>

            <p class="message">
                Thank you for saying YES! 🥰
            </p>

            <p>
                Dili napo ko magpabuyag😭. 💕
            </p>

            <p>
                Iloveyousoomuch po🫰🫶🥹. ✨
            </p>

            <button class="back" onclick="goToPage1()">
                ← Back
            </button>

        </div>

    </div>


    <script>

        function goToPage2() {
            document.getElementById("page1").classList.remove("active");
            document.getElementById("page2").classList.add("active");
        }

        function goToPage1() {
            document.getElementById("page2").classList.remove("active");
            document.getElementById("page1").classList.add("active");
        }

        function sayNo() {
            document.getElementById("noMessage").innerHTML =
                "Diko mo sugot😭😭😭😭😭.";
        }

    </script>

</body>
</html>
