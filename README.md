# hiii
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Mo ❤️</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe4e1;
            padding: 50px;
        }
        .container {
            max-width: 500px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .hidden {
            display: none;
        }
        .yes {
            background-color: #ff69b4;
            color: white;
        }
        .no {
            background-color: #808080;
            color: white;
        }
    </style>
</head>
<body>

<div class="container">
    <h2 id="question">Do you love me?</h2>
    <button class="yes" onclick="nextQuestion(1, 'Good boy, I love you too Mo')">Yes Mommy</button>
    <button class="no" onclick="nextQuestion(1, 'I know you clicked this bc you wanted to see what I wrote')">No I don’t</button>
    
    <div id="next" class="hidden">
        <h2 id="question2">Can you touch me?</h2>
        <button class="yes" onclick="nextQuestion(2, 'Touch me')">Yes Mommy</button>
        <button class="yes" onclick="nextQuestion(2, 'Touch me')">Yes Mommy</button>
    </div>
    
    <div id="final" class="hidden">
        <h2 id="question3">I love you Mo</h2>
        <button class="yes" onclick="nextQuestion(3, 'So dry?')">I love you too</button>
        <button class="yes" onclick="nextQuestion(3, 'Good boy')">I love you too Mommy</button>
        <button class="yes" onclick="nextQuestion(3, 'Turns me on')">I love you Ma</button>
    </div>
    
    <h3 id="response" class="hidden"></h3>
</div>

<script>
    function nextQuestion(step, message) {
        document.getElementById("response").innerText = message;
        document.getElementById("response").classList.remove("hidden");

        if (step === 1) {
            document.getElementById("next").classList.remove("hidden");
        } else if (step === 2) {
            document.getElementById("final").classList.remove("hidden");
        }
    }
</script>

</body>
</html>
