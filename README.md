# INFO2001-Cosolaptrinhweb
bài 1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Larva Registration</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .header img {
            width: 100%;
            height: auto;
        }

        .logo {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 20px 0;
        }

        .logo img {
            width: 80px;
            height: 80px;
        }

        .logo h1 {
            margin-left: 10px;
            font-size: 36px;
            color: #4CAF50;
        }

        .info {
            text-align: center;
            margin-bottom: 30px;
        }

        .info h2 {
            font-size: 24px;
            margin: 10px 0;
        }

        .info p {
            font-size: 16px;
            color: #333;
        }

        form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 30px;
        }

        form input {
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 5px;
            width: 100%;
        }

        .submit-btn {
            grid-column: 1 / 3;
            padding: 15px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
        }

        .submit-btn:disabled {
            background-color: #ccc;
            cursor: not-allowed;
        }

        .login {
            text-align: center;
            font-size: 16px;
        }

        .login a {
            color: #4CAF50;
            text-decoration: none;
        }

        .footer {
            text-align: center;
            margin-top: 20px;
        }

        .footer a {
            color: #333;
            text-decoration: none;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <img src="header-image.jpg" alt="Header Image">
    </div>

    <div class="logo">
        <img src="logo.png" alt="Logo">
        <h1>Larva</h1>
    </div>

    <div class="info">
        <h2>This is not a real online service!</h2>
        <p>You know you need something like this in your life to help you realize your deepest dreams. Sign up now to get started.</p>
        <p>You <em>know</em> want to</p>
        <h2>Let's do this</h2>
    </div>

    <form action="submit_form.php" method="POST">
        <input type="text" name="first_name" placeholder="FIRST NAME" required>
        <input type="text" name="last_name" placeholder="LAST NAME" required>
        <input type="email" name="email" placeholder="EMAIL" required>
        <input type="tel" name="phone_number" placeholder="PHONE NUMBER" required>
        <input type="password" name="password" placeholder="PASSWORD" required>
        <input type="password" name="confirm_password" placeholder="CONFIRM PASSWORD" required>
        <button type="submit" class="submit-btn" disabled>Create Account</button>
    </form>

    <div class="login">
        Already have an account? <a href="login.html">Log in</a>
    </div>

    <div class="footer">
        <img src="footer-image.jpg" alt="Footer Image" style="width: 100%; height: auto;">
        <p>Made by <a href="https://nglarva.github.io/form-register-odin/">NgoLarva</a></p>
    </div>
</div>

<script>
    // Enable the submit button when all fields are filled
    const form = document.querySelector('form');
    const submitBtn = document.querySelector('.submit-btn');
    const inputs = form.querySelectorAll('input');

    inputs.forEach(input => {
        input.addEventListener('input', () => {
            const allFilled = Array.from(inputs).every(input => input.value);
            submitBtn.disabled = !allFilled;
        });
    });
</script>

</body>
</html>
BÀI 22
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Styling Methods</title>
    <!-- External CSS link -->
    <link rel="stylesheet" href="styles.css">
    <style>
        /* Internal CSS method */
        .internal {
            background-color: green;
            color: white;
            font-size: 20px;
            padding: 10px;
            margin: 20px 0;
        }
    </style>
</head>
<body>

    <h1 class="external">Style me via the external method!</h1>

    <p class="internal">I would like to be styled with the internal method, please.</p>

    <button style="background-color: orange; color: black; border: 1px solid gray; padding: 10px;">
        Inline Method
    </button>

</body>
</html>

