# RGB Colour Picker
https://github.com/KritikaTri/Hackproject1/

## The Project

A game to test a users knowledge of colour codes and improve their colour selection skills. The game displays to the user a selection of randomly generated colour tiles, alongside a single colour code, and asks the user to select the correct tile. Users can play the game on easy or hard mode (3 or 6 tiles), as well as having the ability to have the code displayed in either hexidecimal or RGB code.

![ScreenShot](http://res.cloudinary.com/jamesriall/image/upload/v1513605311/color-game-image_rmhd2k.png)

## The Logic

Whenever the page loads of a new round of the game is started I generate a set of new RGB color code by generating 3 sets of random numbers between 0 and 255 and storing them in an array. The length of this array is either 3 or 6 depending on the difficulty of the game, which can be selected by the user. I also generate a random number between 0 and the length of the array -1 which determines which box's code will be displayed on screen as the correct answer to the game. The numbers generated are used to change the CSS background colors of the individual boxes displayed to the user for selection.

When a user clicks on a particular square a function determines whether the square being clicked on has the same array index as the number stored as the correct answer value. If the answer is incorrect, the color fades out and a 'TRY AGAIN' message is displayed, if the answer is correct then I use CSS to display all of the boxes as that correct color and display a 'CORRECT!!!' message to the user.

Users have the ability to generate a new set of colours, change the difficulty and also change the game from testing knowledge of RGB codes to testing knowledge of Hex code (hexConverter function on line 18 of the index.js file).
