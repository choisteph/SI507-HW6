# JavaScript assignment

## Names of people you have worked with on this assignment
* **Stephanie Choi (stchoi)**
* Big thanks to my friend Jenny Wang (wjenny), alumni of the UMich LSA CS program, who helped explain and talk me through approaches for the last jQuery question

## Questions & code instructions

### The first questions address the `jsPracticeLab.html` file.

* **What does a code comment look like in JavaScript? What character/s do you have to put before a comment?**

two slashes //

* **Explain what needs to happen to get a JavaScript program to "run", given the JavaScript you've seen in this assignment.**

scripts run when they are called in the HTML

* **What functions in JavaScript seem to be similar in function to the `print` function in Python? (There are two.) Why might you use one and not the other? Explain briefly.**

console.log will display something in the console on a browser
alert will display something as a popup window on a browser

console.log is good for tracking whether or not things have happened. a user won't see these messages unless they go looking for it in inspect element

alert is good for letting a user know immediately if something is happening

* **What code would have to comment out to get rid of the pop-up box when you load the page? (Related to the last question.) Do that in the code file, and then, add code so that a text box will appear that contains the current date and time! *HINT:* Look through the rest of the code first...**

get rid of the "Hello" in alert()
in the alert, write new Date() instead

(i commented this out because it was getting annoying to have this show up every time i tried to load the page)


* **How can you put your own name at the top where it currently says "A name"? Explain very briefly how to do so, and replace `A name` in the web page with your own name.**

use the existing document.querySelector statement that modifies the 'h1' and adjust the innerHTML with your name as a string

* **What does the word `document` represent in this code? Explain briefly.**

document represents the page

* **What is happening in line 12 (
		`document.querySelector('#items').innerHTML = document.getElementsByTagName('li').length`
)? Explain, briefly (<= 2 sentences).**

for this page, get all the items with the ID "items" and replace the text associated with this item to the length of all items with the class 'li'

* **What color would the background of this page be <u>if there were no JavaScript in this page</u>?**

 white, because there is no style code in HTML associated with a background color value

* **Why are there a couple of gray boxes on the screen with a different colored border? How could you edit this code to make them a different color? Explain briefly. Then edit the code to make those boxes some shade of blue, of your choosing.**

they're styled in the CSS according to their identity as a member of class (paragraph).
going through and adjusting the background-color hex and border hex codes will change.

* **Edit the code so that, if you highlight `McGill University` and copy it, you see the text `O Canada` near the bottom of the page. Briefly explain why you made the edits that you did -- how did you know/figure out what to do?**

define new function copyGill that does the same stuff copyFunction does (add text to the div with ID cheer) but change the innerHTML to the string "O Canada"

go into the list item for McGill and add function for oncopy and have it run the function for copyGill.

* **In the original code, when you click the button that says `Wow`, you see a text box! Wow. Explain briefly in your own words why the following code causes that to happen:**

```js
function handleClick(){
	alert("hello");
}
```

when called, cause an alert box to appear that says hello

**and**

```js
<button onclick=handleClick() id="wow-button">Wow</button>
```

define a button with ID "wow-button". give it an action onclick (react on click), and do the function handleClick


* **Knowing what you learned from the previous question, add code/markup to the `jsPracticeLab.html` file *so that* there is a button with the text `Spring Equinox 2019` on it somewhere on the page, and when that button is clicked, a text box containing the text `March 20, 2019` appears. (There's no function -- that I am aware of -- to automatically get this info, you've got to type it yourself.)**




### The next few questions address the `jquerylib_submit_example.html` file.

* **Check out the file `jquerylib_submit_example.html`. This is an example of code that uses a package called `jQuery` (and this will need you to have an internet connection to run it properly, although the other file does not). Check out resources above for more on jQuery!**

ok!

* **When you enter input that isn't valid, you see an error that is red. Why is the error in red? Why is the response for valid inputs blue?**

the CSS says to style things with the p class 'error' with red text color
the CSS says to style things with the p class 'good' with blue text color

jQuery returns each `<p>` element according to whether or not the input is valid or not

* **What is this line `var regex = /^[a-zA-Z]+$/;` helping with? And if you googled something to figure that out, what did you google, and what, briefly, did you learn? (If you didn't need to google, you can leave that out, but explain briefly what that line is helping the program do, anyway.)**

[According to this Stack Overflow thread](https://stackoverflow.com/questions/2790813/regular-expression-a-za-z-or-a-za-z), when the carot appears outsides of the brackets, match the beginning of the line/string with a letter of the alphabet (check lower and upper cases)

[And according to this Stack Overflow thread](https://stackoverflow.com/questions/26722496/regex-difference-between-a-za-z-vs-a-za-z), $ marks the end of a string, + means one or more. so this statement is the string starts with and contains an alphabet letter and has one or more alphabet characters before the string ends.

So I think this is helping the program determine if the string fits the criteria: one word, letters only



* **What's different about the syntax of conditional statements in JavaScript, compared to Python?**

JS uses if (conditional statement) {things to do};
parentheses, curly brackets, and semicolons

Python uses indents.
if conditional statement
	things to do


* **What do you think the `10000` refers to in the code `.fadeOut(10000)`?**

looks like the speed in milliseconds for the message to fade out.

* **What do you think is going on with the following code at the beginning of the program? Note that the most important thing to do for answering this question is to be thoughtful and clear, not to be absolutely correct:**

```js
$(document).ready(function(){
    $("form").submit(function(event){
		});
});
```
(added the closers to have this display properly)

When the document (html stuff) is done loading, do the function:
When the "form" item does the submit event, run the function.

* **Add some code to the `jquerylib_submit_example.html` file so that, if the input is valid and is specifically the text `hello`, rather than the visible output being `Nice!` in blue, the visible output should be `Hello to you too!`, also in blue, just like `Nice!` is.**
	* *HINT:* You'll have to make some changes to the conditional statement, and possibly look up some JavaScript conditional syntax. You'll also need to look carefully at what generates visible output right now.
