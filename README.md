<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Huma - Coming Soon</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Apercu:ital,wght@0,700&display=swap'); /* Attempt to load Apercu Bold from Google Fonts (if available). If not, fall back to system fonts below. */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            min-height: 100vh;
            width: 100%;
            background-color: #f0f0f0; /* Clean, light gray background */
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .header {
            text-align: center;
            padding: 60px 20px 20px;
            background: rgba(240, 240, 240, 1); /* Solid white background for header */
        }

        h1 {
            color: #333;
            font-family: 'Apercu', Arial Black, Helvetica Neue, sans-serif;
            font-weight: 700;
            font-size: 48px;
            margin-bottom: 20px;
            letter-spacing: 2px; /* Spreads out the letters (positive value) instead of -5px */
        }

        .content {
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
            background: rgba(240, 240, 240, 1); /* Solid white background for content */
        }

        .social-button {
            margin-bottom: 20px;
        }

        /* Instagram Button Styles */
        .instagram-btn {
            font-size: 16px;
            padding: 1em 3.3em;
            cursor: pointer;
            transform: perspective(200px) rotateX(15deg);
            color: white;
            font-weight: 900;
            border: none;
            border-radius: 5px;
            background: linear-gradient(
                0deg,
                rgba(63, 94, 251, 1) 0%,
                rgba(70, 135, 252, 1) 100%
            );
            box-shadow: rgba(63, 94, 251, 0.2) 0px 40px 29px 0px;
            will-change: transform;
            transition: all 0.3s;
            border-bottom: 2px solid rgba(70, 135, 252, 1);
        }

        .instagram-btn:hover {
            transform: perspective(180px) rotateX(30deg) translateY(2px);
        }

        .instagram-btn:active {
            transform: perspective(170px) rotateX(36deg) translateY(5px);
        }

        .coming-soon-section {
            text-align: center;
            margin-bottom: 20px;
        }

        .coming-soon {
            color: #666;
            font-size: 32px;
            font-weight: bold;
        }

        .notify-text {
            color: #666;
            font-size: 18px;
            margin-top: 5px;
        }

        .form-section {
            width: 100%;
            max-width: 700px; /* Increased from 500px to make the form box longer (wider) */
        }

        /* Uiverse.io Form Styles */
        .form {
            position: relative;
            display: flex;
            flex-direction: column;
            gap: 10px;
            padding: 20px;
            background: linear-gradient(to bottom, #666666, #999999);
            border-radius: 10px;
            overflow: hidden;
            perspective: 1000px;
            transform-style: preserve-3d;
            transform: rotateX(-10deg);
            transition: all 0.3s ease-in-out;
            box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px, rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
            animation: form-animation 0.5s ease-in-out;
        }

        @keyframes form-animation {
            from {
                transform: rotateX(-30deg);
                opacity: 0;
            }
            to {
                transform: rotateX(0deg);
                opacity: 1;
            }
        }

        .input {
            padding: 10px;
            border-radius: 5px;
            background-color: transparent;
            transition: border-color 0.3s ease-in-out, background-color 0.3s ease-in-out, transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            transform-style: preserve-3d;
            backface-visibility: hidden;
            color: rgb(255, 255, 255);
            border: 2px solid #999999;
            box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px, rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
            width: 100%; /* Ensures inputs stretch to full width of form */
        }

        .input::placeholder {
            color: #fff;
        }

        .input:hover,
        .input:focus {
            border-color: #999999;
            background-color: rgba(255, 255, 255, 0.2);
            transform: scale(1.05) rotateY(20deg);
            box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.3);
            outline: none;
        }

        button:not(.instagram-btn) {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #999999;
            color: #fff;
            font-size: 16px;
            cursor: pointer;
            transform-style: preserve-3d;
            backface-visibility: hidden;
            transform: rotateX(-10deg);
            transition: all 0.3s ease-in-out;
            box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px, rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
            width: 100%; /* Ensures button stretches to full width of form */
        }

        button:not(.instagram-btn):hover {
            background-color: #666666;
            font-size: 17px;
            transform: scale(1.05) rotateY(20deg) rotateX(10deg);
            box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px, rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;
        }

        #response {
            text-align: center;
            margin-top: 20px;
            color: #666;
            font-size: 16px;
        }

        .footer {
            text-align: center;
            padding: 20px;
            background: rgba(240, 240, 240, 1); /* Solid light gray background for footer */
            color: #999;
            font-size: 14px;
        }
    </style>
</head>
<body>
    
    <div class="header">
        <h1>Huma</h1>
    </div>

    <div class="content">
        <div class="social-button">
            <a href="https://www.instagram.com/humadating/" target="_blank">
                <button class="instagram-btn">Instagram</button>
            </a>
        </div>
        <div class="coming-soon-section">
            <div class="coming-soon">Coming Soon</div>
            <div class="notify-text">Get notified when we launch</div>
        </div>
        <div class="form-section">
            <form id="notifyForm" class="form" action="https://formsubmit.co/el/covewu" method="POST">
                <input class="input" type="email" name="email" placeholder="Enter your email" required>
                <textarea class="input" name="message" placeholder="Optional message"></textarea>
                <input type="hidden" name="_next" value="https://yourwebsite.com/thanks.html">
                <input type="hidden" name="_subject" value="Huma Launch Notification Signup">
                <input type="hidden" name="_cc" value="humadating@gmail.com">
                <input type="hidden" name="_template" value="table">
                <button type="submit">Notify Me</button>
            </form>
            <div id="response"></div>
        </div>
    </div>

    <div class="footer">
        © 2025 Huma. All rights reserved.
    </div>

    <script>
        document.getElementById('notifyForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const form = this;
            const responseDiv = document.getElementById('response');
            
            responseDiv.textContent = 'Submitting...';
            
            fetch(form.action, {
                method: 'POST',
                body: new FormData(form)
            })
            .then(response => {
                if (response.ok) {
                    return response.json();
                } else {
                    throw new Error('Form submission failed with status: ' + response.status);
                }
            })
            .then(data => {
                responseDiv.textContent = 'Thank you! We\'ll notify you when Huma launches.';
                form.reset();
                console.log('Form submission successful:', data);
            })
            .catch(error => {
                responseDiv.textContent = 'Something went wrong. Please try again.';
                console.error('Form submission error:', error);
            });
        });
    </script>
</body>
</html>
