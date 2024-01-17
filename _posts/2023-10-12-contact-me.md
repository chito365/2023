---
layout: post
title: Contact Oscar .... Kontakta Oscar
subtitle: Contact Oscar .... Kontakta Oscar
gh-repo: chito365/2023
gh-badge: [star, fork, follow]
tags: [contact]
comments: true
---


**Contact Oscar .... Kontakta Oscar**

## Use this form ...


  <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .form-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }

        input,
        textarea {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            box-sizing: border-box;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: #4caf50;
            color: #fff;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        .error-message {
            color: red;
            margin-bottom: 10px;
        }
    </style>

    <div style="text-align: center; margin-top: 50px;">
        <h2>Contact Us</h2>
        <div style="background-color: #fff; padding: 20px; border-radius: 8px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); width: 300px; margin: 0 auto;">

            <form id="contactForm">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="subject">Subject:</label>
                <input type="text" id="subject" name="subject" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>

                <p style="color: red; margin-bottom: 10px;" id="errorMessage"></p>

                <button type="button" onclick="submitForm()">Submit</button>
            </form>

        </div>
    </div>

    <script>
        function submitForm() {
            var email = document.getElementById('email').value;
            var subject = document.getElementById('subject').value;
            var message = document.getElementById('message').value;
            var errorMessage = document.getElementById('errorMessage');

            if (email.trim() === '' || subject.trim() === '' || message.trim() === '') {
                errorMessage.textContent = 'Please fill in all fields.';
            } else {
                var mailto = 'oscahchitoh@gmail.com';
                var mailSubject = 'New Contact Form Submission';
                var mailBody = 'Email: ' + email + '\nSubject: ' + subject + '\nMessage: ' + message;

                console.log('Email:', email);
                console.log('Subject:', subject);
                console.log('Message:', message);

                document.getElementById('contactForm').reset();
                errorMessage.textContent = '';
                
                // You can now use the mailto, mailSubject, and mailBody variables to send the data to the server.
                // In a real-world scenario, you would use AJAX or another method to send data to the server.
            }
        }
    </script>