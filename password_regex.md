# Password Regular Expression

Patterns

Characters	Meaning:

* \d	Checks for a digit match e.g: it returns 2 in “U2”.
* \W	Checks for a special character e.g: returns % in “2%”.
* x{n,}	Checks for at least n terms from the preceding term x e.g: O{2,} does not return anything in “BOY” but returns all Os in GOOOOOAL!.
* xIy	Matches either x or y in a string
* [^vet]	A negated set. Doesn’t check for anything included in the range ie Does not check for vet in “veterinary”
* [A-Za-z0-9]	Checks all alphanumeric characters
* [a-z]	Checks for lowercase letters
* [A-Z]	Checks for uppercase letters
* x(?=y)	Returns x if and only if it is followed by y
* .	Checks for any single character except line terminators
* x*	Checks for x 0 or more times

RegEx for testing password strength
We are going to check the strength of a password that a user enters based on the following rules:

* The password is at least 8 characters long (?=.{8,}).

* The password has at least one uppercase letter (?=.*[A-Z]).

* The password has at least one lowercase letter (?=.*[a-z]).

* The password has at least one digit (?=.*[0-9]).

* The password has at least one special character ([^A-Za-z0-9]).

* The password doesn't allow (?!.*[]).


Fonte: https://www.section.io/engineering-education/password-strength-checker-javascript/ <br>
Complementar: https://regexlib.com/Search.aspx?k=passwo