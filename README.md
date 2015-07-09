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


ctf.infosecinstitute.com/ctf2/exercises/ex13.php?redirect=%0d%0a%20CostumHeader:INJECTED
