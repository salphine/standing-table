<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SALPHINE QUIZ</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #eaecef;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            background: white;
            margin: auto;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            font-size: 24px;
        }

        fieldset {
            border: none;
            padding: 10px 0;
        }

        legend {
            font-weight: bold;
            font-size: 18px;
        }

        label {
            display: block;
            margin-top: 10px;
            font-weight: bold;
        }

        input[type="text"],
        input[type="email"],
        input[type="date"] {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        .question {
            margin-top: 20px;
        }

        .question p {
            font-weight: bold;
        }

        .question label {
            font-weight: normal;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .submit-btn {
            display: block;
            width: 100%;
            background-color: #007BFF;
            color: white;
            border: none;
            padding: 10px;
            font-size: 18px;
            border-radius: 5px;
            margin-top: 20px;
            cursor: pointer;
        }

        .submit-btn:hover {
            background-color: #0056b3;
        }

        .result {
            text-align: center;
            font-size: 20px;
            font-weight: bold;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>SALPHINE  QUIZ</h1>

        <fieldset>
            <legend>Student Info</legend>
            <label for="name">Name:</label>
            <input type="text" id="name">

            <label for="email">Email:</label>
            <input type="email" id="email">

            <label for="dob">Date of Birth:</label>
            <input type="date" id="dob">
        </fieldset>

        <hr>

        <div class="question">
            <p>Question #1</p>
            <p>The &lt;legend&gt; element represents a caption for the content of its parent &lt;fieldset&gt; element.</p>
            <label><input type="radio" name="q1" value="true"> True</label>
            <label><input type="radio" name="q1" value="false"> False</label>
        </div>

        <div class="question">
            <p>Question #2</p>
            <p>A &lt;label&gt; element nesting an input element is required to have a <code>for</code> attribute with the same value as the input's <code>id</code>.</p>
            <label><input type="radio" name="q2" value="true"> True</label>
            <label><input type="radio" name="q2" value="false"> False</label>
        </div>

        <div class="question">
            <p>Question #3</p>
            <p>Which CSS property is used to change the text color of an element?</p>
            <label><input type="radio" name="q3" value="color"> color</label>
            <label><input type="radio" name="q3" value="background-color"> background-color</label>
            <label><input type="radio" name="q3" value="text-color"> text-color</label>
        </div>

        <div class="question">
            <p>Question #4</p>
            <p>What does the <code>alt</code> attribute in an &lt;img&gt; tag do?</p>
            <label><input type="radio" name="q4" value="Adds a caption"> Adds a caption</label>
            <label><input type="radio" name="q4" value="Provides alternative text for accessibility"> Provides alternative text for accessibility</label>
            <label><input type="radio" name="q4" value="Changes the image size"> Changes the image size</label>
        </div>

        <div class="question">
            <p>Question #5</p>
            <p>Which CSS property is used to create space between elements?</p>
            <label><input type="radio" name="q5" value="margin"> margin</label>
            <label><input type="radio" name="q5" value="padding"> padding</label>
            <label><input type="radio" name="q5" value="spacing"> spacing</label>
        </div>

        <button class="submit-btn" onclick="checkAnswers()">Submit</button>

        <p class="result" id="result"></p>
    </div>

    <script>
        function checkAnswers() {
            let name = document.getElementById("name").value;
            let email = document.getElementById("email").value;
            let dob = document.getElementById("dob").value;

            if (!name || !email || !dob) {
                alert("Please fill in all student details before submitting.");
                return;
            }

            let correctAnswers = {
                q1: "true",
                q2: "true",
                q3: "color",
                q4: "Provides alternative text for accessibility",
                q5: "margin"
            };

            let score = 0;
            let totalQuestions = Object.keys(correctAnswers).length;

            for (let key in correctAnswers) {
                let selected = document.querySelector(`input[name="${key}"]:checked`);
                if (selected && selected.value === correctAnswers[key]) {
                    score++;
                }
            }

            let resultText = `You scored ${score} out of ${totalQuestions}.`;
            if (score === totalQuestions) {
                resultText += " 🎉 Excellent!";
            } else if (score >= 3) {
                resultText += " 😊 Good job!";
            } else {
                resultText += " 😢 Try again!";
            }

            document.getElementById("result").textContent = resultText;
        }
    </script>

</body>
</html>
