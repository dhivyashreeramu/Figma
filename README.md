# Ex09 Event Registration Web Application
# Date:06.10.2025
# AIM:
To design, develop and deploy a web application for event registration.

# DESIGN STEPS:
## Step 1:
Create a new frame.

## Step 2:
Select any one preset size of your choice.

## Step 3:
Select the shapes you need.

## Step 4:
Import images as needed.

## Step 5:
Create pages based on your need and link them.

## Step 6:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# DESIGN TOOL:
Figma

# CODE:
```<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Event App</title>
  <style>
    body {
      background-color: #f3f4f6;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 1rem;
      margin: 0;
    }
    .container {
      width: 100%;
      max-width: 24rem;
      background-color: white;
      border-radius: 1.5rem;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      height: 720px;
      padding: 1.5rem;
      box-sizing: border-box;
    }
    .screen {
      display: none;
    }
    .screen.active {
      display: block;
    }
    .button {
      background-color: #3b82f6;
      color: white;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 0.5rem;
      cursor: pointer;
      margin-top: 1rem;
    }
    .button:hover {
      background-color: #2563eb;
    }
  </style>
</head>
<body>

  <div class="container">
    <!-- Home Screen -->
    <div id="homeScreen" class="screen active">
      <h2>Welcome to the Event App</h2>
      <button class="button" onclick="showScreen('eventsScreen')">Login</button>
      <button class="button" onclick="showScreen('eventsScreen')">Register</button>
    </div>

    <!-- Events Screen -->
    <div id="eventsScreen" class="screen">
      <h2>Select an Event</h2>
      <ul>
        <li><button class="button" onclick="selectEvent('Event A')">Event A</button></li>
        <li><button class="button" onclick="selectEvent('Event B')">Event B</button></li>
        <li><button class="button" onclick="selectEvent('Event C')">Event C</button></li>
      </ul>
      <button class="button" onclick="showScreen('homeScreen')">Back</button>
    </div>

    <!-- Registration Screen -->
    <div id="registrationScreen" class="screen">
      <h2>Register for <span id="eventName"></span></h2>
      <form onsubmit="submitForm(event)">
        <input type="text" placeholder="Your Name" required /><br/><br/>
        <input type="email" placeholder="Your Email" required /><br/><br/>
        <button type="submit" class="button">Submit</button>
      </form>
      <button class="button" onclick="showScreen('eventsScreen')">Back</button>
    </div>

    <!-- Thank You Screen -->
    <div id="thankYouScreen" class="screen">
      <h2>Thank you for registering!</h2>
      <button class="button" onclick="showScreen('eventsScreen')">Back to Events</button>
      <button class="button" onclick="showScreen('homeScreen')">Back to Home</button>
    </div>
  </div>

  <script>
    function showScreen(screenId) {
      document.querySelectorAll('.screen').forEach(screen => {
        screen.classList.remove('active');
      });
      document.getElementById(screenId).classList.add('active');
    }

    function selectEvent(eventName) {
      document.getElementById('eventName').textContent = eventName;
      showScreen('registrationScreen');
    }

    function submitForm(e) {
      e.preventDefault();
      showScreen('thankYouScreen');
    }
  </script>
</body>
</html>
```

# OUTPUT:
home page:
![HOME PAGE](<Screenshot (55).png>)
REGISTER FORM:

![REGISTER](<Screenshot (56).png>)
LOGIN :

![LOGIN](<Screenshot (57).png>)



# RESULT:
The program to design, develop and deploy a web application for event registration is completed successfully.
