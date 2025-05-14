<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Secret Access</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            background-color: black;
            color: white;
            text-align: center;
            font-family: Arial, sans-serif;
            position: relative;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .action-button {
            background-color: gray;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            margin: 10px;
        }

        .action-button:hover {
            background-color: white;
            color: black;
        }

        .download-button {
            position: absolute;
            bottom: 20px;
            background-color: blue;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
        }

        .download-button:hover {
            background-color: white;
            color: blue;
        }
    </style>
</head>
<body>
    <h1>Welcome to the Secret Zone</h1>

    <!-- Creating 10 buttons for secret access -->
    <div class="button-container">
        <button class="action-button" onclick="verifyPassword()">Access More 1</button>
        <button class="action-button" onclick="verifyPassword()">Access More 2</button>
        <button class="action-button" onclick="verifyPassword()">Access More 3</button>
        <button class="action-button" onclick="verifyPassword()">Access More 4</button>
        <button class="action-button" onclick="verifyPassword()">Access More 5</button>
        <button class="action-button" onclick="verifyPassword()">Access More 6</button>
        <button class="action-button" onclick="verifyPassword()">Access More 7</button>
        <button class="action-button" onclick="verifyPassword()">Access More 8</button>
        <button class="action-button" onclick="verifyPassword()">Access More 9</button>
        <button class="action-button" onclick="verifyPassword()">Access More 10</button>
    </div>

    <!-- Download Button -->
    <button class="download-button" onclick="downloadFile()">Download File</button>

    <script>
        function verifyPassword() {
            const password = prompt("Enter the secret password:");
            const correctPassword = "123"; // Modify the password if needed

            if (password === correctPassword) {
                alert("Access Granted! Redirecting...");
                window.location.href = "https://www.google.com"; // Change the link as needed
            } else {
                alert("Access Denied! Incorrect password.");
            }
        }

        function downloadFile() {
            const link = document.createElement("a");
            link.href = "your-file.pdf"; // Change this to the actual file path
            link.download = "Secret_File.pdf"; // Rename the file as needed
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        }
    </script>
</body>
</html>
