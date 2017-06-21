# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for?
Html is a markup language for defining the presentation structure for web based applications
2. What is the difference between an ID and a class? 
ID is a more specific categorization used for only one tag.
Class can group one or many Html tags to be styled in css together.
3. What does it mean to write "semantic" HTML?
Semantic HTML is the use of HTML markup to reinforce the meaning of the information in webpages and web applications rather than merely to define its presentation or look. * Being Specific *

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
<p class = "highlight"> Watch Out! </p>
2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img src= "profile-picture.jpg" alt= "profile picture">
3. Write a link tag that links to http://google.com.
<a href="http://google.com">Its Google</a>
5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).
<!DOCTYPE html>
<html>
  <head>
    <script src=main.js></script>
    <title></title>
  <body>
    <p><link rel=stylesheet type=text/css href= main.css> </p>
  </body>
  </html>
6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
8. Write a numbered list in HTML and list three of your favorite books.
<ol>
  <li>Daring Greatly</li>
  <li>Blitzed</li>
  <li>The Checklist Manifesto</li>
</ol>
9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for?
CSS is used to Style Html documents.
2. What is the CSS box model?
All content is seperated into individual content boxes. width, height, padding, border, margin
3. What's the difference between margin and padding?
Margin refers to the spacing between content boxes.
Padding refers to the spacing within content boxes but between content.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.

h1{
  color: #ff0000;
}

2. Write a CSS rule to make the background color of the link with `class="btn"` blue:

.btn {
 background-color: #0000ff;
}

  ```html
  <a href="#" class="btn">Learn more</a>
  ```

3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

.jumbotron p {
  font-size: 20px;
}
  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```

## JavaScript

### Questions

1. What is a function? What are they used for?
Programs which will evaluate and perform tasks. – reusable set of programming instructions that can be modified with inputs
2. What is the difference between `==` and `===`?
console.log(5 === "5"); // strict comparison - compares both value and data type
console.log(5 == "5"); // loose comparison - compares only value
3. What is the difference between global and local scope variables?
A global variable can apply to all of the code. 
A local scope variable will only apply within the subsect of code in which it was written.
4. What is a boolean value?
True, False
5. What is an array?
An array is a data structure that contains a list of values

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.

var myName = "Matt Nichols";

2. Write a loop that logs the numbers 1 through 10 to the console.

for (num = 1; num <= 10; num++){
  console.log(num);
}

3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".

if (score > 3 && lives > 0){
  alert("You Win!");
}

4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.

function sayHello(name){
  console.log("Hello, " + name + "!");
}

sayHello("Matt Nichols");

5. What would the following script log to the console?

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```
  **Friday, Friday** 


6. What would the following script log to the console?


  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```
  10

7. What would the following script log to the console?

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name + " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name + " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```
  Hello Sarah ! Goodbye Sarah !
  
**This is where my Headache started** -------------------------------------------------------------------------------------

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.
                                          
var findLongestWord = function(words) {
  var longestWord;
  for (var i = 0; i < words.length; i++) {
    if (longestWord) {
        if (words[i].length > longestWord.length) {
          longestWord = words[i];
        }
    } else {
      longestWord = words[i];
    }
  }
  return longestWord;
};

var words = ["Curiosity", "Killed", "Cat"];
var longestWord = findLongestWord(words);
console.log(longestWord);

9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
var sum = function(array) {
  var length = array.length;
  var total = 0;
  for (i = 0; i < length; i++) {
    total += array[i];
  }
  return total;
};



10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.

var findVowel = function(letter) {

    var vowels = ["a", "e", "i", "o", "u"];

    for(var i = 0; i < vowels.length; i++){
     if(letter === vowels[i]){
            return true;
        }
        }
  
    return false;
   
      };

11. Write the correct line to make `"Woof!"` show up in the console based on this script:

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```
  pet.speak();

12. Using the same script as above, write the correct line to log the dog's name to the console.

console.log(pet.name);

## Command Line

### Questions

1. What is the command line and what is it used for?
Command line is a text based interface used to navigate and and edit your computer's directories and files.
2. What does the command `ls` do?
ls - lists files in current directory 
3. What does the command `pwd` do?
pwd - Lists current directory
4. What does the following command do: `cd my-cool-project`
Change's your location to the directory named my-cool-project

### Exercises

1. Write the command to make a new directory called "my-cool-project".
mkdir my-cool-project
2. Write the command to create a file called "index.html".
touch index.html
3. Write the command to delete a file called "main.css".
rm main.css

## Git

### Questions

1. What is Git and what is it used for?
Git is a tool for organizing and navigating files.
2. What's the difference between a local repository and a remote repository?
Local repository refers to the repository stored on your computer, you do not need to be online to access it.
Remote repository refers to a repository that is stored over the internet via a service such as Github, you must be online to access it.

### Exercises

1. Write the command that you would use to create a new local Git repository.
gitinit
2. Write the command to stage a file called `index.html` to be committed.
git add index.html
3. Write the command to view the current status of the git repository.
git status
