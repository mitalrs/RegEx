# RegEx:(Regular expressions)-
**Regular expressions** are used in programming languages to match parts of strings. You create patterns to help you do that matching.

- .test() : If you want to find the word the in the string The dog chased the cat, you could use the following regular expression: /the/. Notice that quote marks are not required within the regular expression.

example:
> let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr);


- i : You can match both cases using what is called a flag. There are other flags but here you'll focus on the flag that ignores case - the i flag. You can use it by appending it to the regex. An example of using this flag is /ignorecase/i. This regex can match the strings ignorecase, igNoreCase, and IgnoreCase.


example:
> let myString = "freeCodeCamp";
let fccRegex = /freeCodeCamp/i; 
let result = fccRegex.test(myString);


- .match() :you have only been checking if a pattern exists or not within a string. You can also extract the actual matches you found with the .match() method.

To use the .match() method, apply the method on a string and pass in the regex inside the parentheses.

example:
> "Hello, World!".match(/Hello/);
let ourStr = "Regular expressions";
let ourRegex = /expressions/;
ourStr.match(ourRegex);
output: Here the first match would return ["Hello"] and the second would return ["expressions"].


Note that the .match syntax is the "opposite" of the .test method you have been using thus far:

> 'string'.match(/regex/);
/regex/.test('string');



-g: To search or extract a pattern more than once, you can use the global search flag: g.

example: 
> let testStr = "Repeat, Repeat, Repeat";
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);

example; i and g:
> let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /Twinkle/ig; // Change this line
let result = twinkleStar.match(starRegex); // Change this line


- . : Sometimes you won't (or don't need to) know the exact characters in your patterns. Thinking of all words that match, say, a misspelling would take a long time. Luckily, you can save time using the wildcard character: .
 The wildcard character . will match any one character. The wildcard is also called dot and period. You can use the wildcard character just like any other character in the regex. For example, if you wanted to match hug, huh, hut, and hum, you can use the regex /hu./ to match all four words.


 example: it matches the strings run, sun, fun, pun, nun, and bun. Your regex should use the wildcard character.

 > let exampleStr = "Let's have fun with regular expressions!";
let unRegex = /.un/; // Change this line
let result = unRegex.test(exampleStr);

