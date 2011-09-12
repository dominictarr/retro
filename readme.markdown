#RETRO
```
   ,,,,,,,,,      ,,,,,,,,,,    ,,,,,,,,,,    ,,,,,,,,,     ,,,,,,,,,  
  /       /|     /        /|   /        /|   /       /|    /       /|
 /       / |    /        / |  /        / |  /       / |   /       / |
|```````|  |   |````````|  | |````````| /  |```````|  |  |````````| |
|   [ ] | /,   |  [:::] | /| |      ,,|/   |   [ ] | /,  |   ,,   | |
|      _|/ \   |  ______|/ |  |     |  |   |      _|/ \  |  [  ]  | | 
|      \  /    |  |;... | /   |     | /    |      \  /   |   ``   | / 
|_______\/     |________|/    |.....|/     |_______\/    |________|/
```
A lib that harkens back to the old days when everything 
was an acronym and you had to shout at the computer to get it to do anything.
 
*RETRO* provides a bold new set of async control flow statesments in _CAPS_.

``` js

retro.IF(test).THEN(function).ELSE(function)

retro.NOT(function)
retro.TRUE //function that calls back true
retro.FALSE //function that calls back false

retro
  .TRY(function)
  .CATCH(function)    // called if try errors
  .PASS(function)     // called if try does not error
  .FINALLY(function)  // called after CATCH/PASS wether or not TRY errored. 
                      // (unless CATCH or PASS errored)

retro
  .TRY(function)
  .FINALLY(function) // CATCH/PASS are optional

retro
  .WHILE(test)       // async test
  .DO(function)      // perform this function

retro
  .DO(function)      // the same, but DO first, then check. 
  .WHILE(test)

retro
  .FOR_EACH(array)
  .DO(function)      // DO this FOR_EACH item in the array

retro.UNTIL(test)    // same as while, but do until test fails
  .DO(function)

retro
  .DO(function)
  .UNTIL(test)

retro
  .OPEN_PANDORA_BOX() // install monkeypatches onto global context

```

*** thinking outloud ***
TRY...CATCH...FINALLY will probably be the most useful. 
because often one does use an async error value to test something.

sync if returns.
