# NotetakingApp

- Created with NodeJS and npm
- With npm, I used Chalk(to get console message colored), fs(to create a file and read data from the file), and yargs(to call function by command with properties) from request library

- In notes.js file, I created functions for read, add, remove, save, load, list
- For loadNotes in notes.js, this function can create a file if not exists with empty array, if exists, it reads data with readfilesync and parsing to JSON
- For removingNote, this function uses the JSON data in loadNotes and match the same title with filter methods and remove it
- For readNote, this function can also find with title name from loadNotes() and console message shows the status with chalk color
- For addNote, this function requires title and body messages to save by pushing the array from loadNotes, if two params not exist, error occurs
- For saveNotes, this function convert JSON to string to save with fs.writefilesync method

- In app.js file, I set the app with yargs that makes user input according to builder in command
- The command is add, remove, read, list
