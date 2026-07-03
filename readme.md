Demo Projects

This is a small collection of little browser projects we built while practicing HTML, CSS, and JavaScript. No frameworks, no libraries, just plain code. Each one is a single HTML file, so we can just open it in a browser and it works right away.

What's inside


Quiz App – a simple quiz with 4 questions about JavaScript basics
Guess the Number – a number guessing game (1 to 100)
Word Counter – a tool that counts words, characters, and sentences as we type


How to run these

We don't need to install anything. Just save any of the files as .html and open it in a browser like Chrome or Firefox. That's it.


1. Quiz App

We get asked 4 questions about basic JavaScript stuff. For each question we pick one of the 4 options. As soon as we click, it shows us if we got it right or wrong (green means correct, red means wrong). Then we hit "Next" to go to the next question. At the end it shows our score and lets us restart.

How the code works:


questions is just a list that holds all our questions, the options, and which one is correct
renderQuestion() shows the current question on the screen
selectOption() runs when we click an answer, checks if it's right, and updates the score
nextQuestion() moves to the next question, or shows the result if we're done
renderResult() shows our final score
restartQuiz() resets everything so we can play again



2. Guess the Number

The game picks a random number between 1 and 100, and we try to guess it in as few tries as possible. After every guess it tells us if we're too high or too low. It also keeps track of how many attempts we made and remembers our best score.

How the code works:


secretNumber is the random number we're trying to guess
checkGuess() runs every time we click "Guess", checks our answer, and gives feedback
restartGame() starts a new round with a new random number
Our best score is saved using localStorage, so it stays even if we close the tab and come back later


Small note: the best score saving only works in a real browser. It won't save in sandboxed preview tools that block browser storage, but the game itself still works fine there.


3. Word Counter

We can type or paste any text into the box, and it shows us live stats: how many words, characters, and sentences we wrote, plus an estimated reading time. There's also an "Analyze Text" button that pretends to do a deeper analysis (with a short fake loading delay) and then tells us the word count again.

How the code works:


updateStats() runs every time we type, and updates all the numbers on screen
countWords() counts words by splitting the text on spaces
countSentences() counts sentences by looking for ., !, or ?
estimateReadTime() guesses how long it would take to read the text out loud
handleAnalyzeClick() runs when we click the button, waits a second (fake delay), then shows the word count again



Why i built these

These were just practice projects to get more comfortable with plain JavaScript, things like handling clicks, updating the page without reloading, and working with the DOM directly, without relying on React or any other library.

Things we might add later


More questions in the quiz
A timer for each quiz question
Sound effects for right/wrong answers
Saving quiz high scores too
A dark mode for the word counter