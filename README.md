# paralysis-detection
early detection of paralysis
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Medical User Details Form</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600&display=swap');
        
        body {
            font-family: 'Open Sans', sans-serif;
            background-color: #e0f7fa;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(135deg, #e0f7fa 40%, #b2dfdb 100%);
            overflow: hidden;
        }

        .container {
            background-color: #ffffff;
            border-radius: 15px;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
            padding: 40px;
            width: 350px;
            text-align: center;
            animation: slideIn 1s ease-out;
            position: relative;
        }

        .container:before {
            content: '';
            position: absolute;
            width: 300px;
            height: 300px;
            background: #80deea;
            top: -100px;
            right: -100px;
            border-radius: 50%;
            z-index: -1;
            animation: pulseAnimation 3s infinite ease-in-out;
        }

        h2 {
            color: #00897b;
            margin-bottom: 20px;
            font-weight: 600;
        }

        label {
            display: block;
            margin: 10px 0 5px;
            color: #004d40;
        }

        input, select {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #80cbc4;
            border-radius: 5px;
            font-size: 16px;
            outline: none;
            background-color: #f1f8e9;
        }

        button {
            padding: 10px 20px;
            background-color: #00796b;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        button:hover {
            background-color: #004d40;
            transform: scale(1.05);
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes pulseAnimation {
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

        /* Responsive Design for Mobile Screens */
        @media (max-width: 600px) {
            body {
                flex-direction: column;
                padding: 20px;
                justify-content: flex-start;
            }

            .container {
                width: 100%;
                padding: 30px;
                margin: 20px 0;
                box-shadow: none;
                border-radius: 10px;
            }

            h2 {
                font-size: 24px;
            }

            input, select {
                font-size: 14px;
                padding: 8px;
            }

            button {
                padding: 12px;
                font-size: 16px;
            }

            .container:before {
                width: 200px;
                height: 200px;
                top: -80px;
                right: -50px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h2><i class="fas fa-heartbeat"></i> Medical User Details Form</h2>
        <form id="userForm">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>

            <label for="gender">Gender:</label>
            <select id="gender" name="gender" required>
                <option value="" disabled selected>Select your gender</option>
                <option value="male">Male</option>
                <option value="female">Female</option>
                <option value="other">Other</option>
            </select>

            <label for="age">Age:</label>
            <input type="number" id="age" name="age" required>

            <label for="marital-status">Marital Status:</label>
            <select id="marital-status" name="marital-status" required>
                <option value="" disabled selected>Select marital status</option>
                <option value="UnMarried">UnMarried</option>
                <option value="married">Married</option>
            </select>

            <label for="smoking-status">Smoking Status:</label>
            <select id="smoking-status" name="smoking-status" required>
                <option value="" disabled selected>Select smoking status</option>
                <option value="non-smoker">Non-Smoker</option>
                <option value="smoker">Smoker</option>
            </select>

            <label for="alcohol-status">Alcohol Status:</label>
            <select id="alcohol-status" name="alcohol-status" required>
                <option value="" disabled selected>Select alcohol status</option>
                <option value="non-drinker">Non-Drinker</option>
                <option value="drinker">Drinker</option>
            </select>

            <label for="blood-group">Blood Group:</label>
            <select id="blood-group" name="blood-group" required>
                <option value="" disabled selected>Select your blood group</option>
                <option value="A+">A+</option>
                <option value="A-">A-</option>
                <option value="B+">B+</option>
                <option value="B-">B-</option>
                <option value="AB+">AB+</option>
                <option value="AB-">AB-</option>
                <option value="O+">O+</option>
                <option value="O-">O-</option>
            </select>

            <label for="language-status">Language Status:</label>
            <select id="language-status" name="language-status" required>
                <option value="" disabled selected>Select language status</option>
                <option value="tamil">Tamil</option>
                <option value="english">English</option>
            </select>

            <button type="submit">Submit</button>
        </form>
    </div>

    <script>
        document.getElementById("userForm").addEventListener("submit", function(event) {
            event.preventDefault();
            alert("Form Submitted Successfully!");

            // You can add form data validation or submission logic here.
        });
    </script>
</body>
</html>
