# Birthday Wishes App 

A simple web application created to celebrate the birthday of a team member.  
The app allows users to submit birthday wishes, stores them in Firebase Realtime Database, and displays them dynamically on the page.  
It also includes animations, audio playback, a Matrix-style background effect, and a confetti effect.

## Features

- Intro screen with a start button
- Firebase Realtime Database integration
- Adding and displaying wishes in real time
- Background audio playback
- Matrix-style animated canvas background
- Confetti animation on wish submission
- Random quote display
- Wish counter
- Responsive layout

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Firebase Realtime Database
- Canvas API
- canvas-confetti library

## Project Structure

index.html # Main application file
mario-type-beat.mp3 # Background audio


## Firebase Configuration

The app uses Firebase Realtime Database.  
Configuration is provided directly in the script block inside the HTML file.

To use your own Firebase instance:
1. Create a Firebase project.
2. Enable Realtime Database.
3. Replace the configuration object:

```js
const firebaseConfig = {
  apiKey: "...",
  authDomain: "...",
  databaseURL: "...",
  projectId: "...",
  storageBucket: "...",
  messagingSenderId: "...",
  appId: "...",
  measurementId: "..."
};


How to Run

Clone or download this repository.

Open index.html in any browser.

Firebase features will work automatically as long as the configuration is correct.

How It Works
Adding a wish

User enters name and message.

Data is sent to Firebase using:
db.ref('wishes').push().set({ name, wish });
Wishes are displayed live using Firebase listeners.

Matrix Effect

Canvas covers the screen.

Random binary characters flow down using timed drawing cycles.

Confetti Effect

Triggered after each wish submission.

Audio

Starts after clicking “Enter” on the intro screen.

Plays in loop at low volume.

Notes

The app is fully client-side (HTML/JS/CSS).

No backend is required.

Firebase handles all data storage.

License

This project is licensed under the MIT License.
