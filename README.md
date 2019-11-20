# CubeSolver
Python code of the CubeSolver project

This is the code of our CubeSolver projet adapted in Python.

**Les explications en français sont en-dessous.**

The explanation of our solving method is epxlained down below (after the french explanation).

## How to use it

To use it launch useSolver.py, it will ask you for a representation of your cube. Here is how it works :

A Rubik's Cube is represented in our code by an array containing 54 integers like this (it's only an example!):
```

[3,0,5,5,0,5,0,4,0,3,2,4,1,3,4,3,1,0,0,3,4,1,4,5,3,0,5,1,0,1,2,1,3,1,1,4,2,4,4,2,2,5,1,4,2,2,2,5,3,5,3,2,0,5]

```
They each reprensent one color of the cube.
You'll need to write this array for the solver to solve your cube, here is how to do it:
- ### Color representation:
  Each color is assigned to a number:
  
  - Yellow = 0
  - Blue = 1
  - Red = 2
  - Green = 3
  - Orange = 4
  - White = 5
  
  The order is not random and is linked to the array reprensentation.
- ### Faces order and representations
  The representation is composed of 6 individual reprensatations of the 6 faces of the Rubik's Cube, considering the previous example:
  ```
  
  [3,0,5,5,0,5,0,4,0] = Yellow face
  [3,2,4,1,3,4,3,1,0] = Blue face
  [0,3,4,1,4,5,3,0,5] = Red face
  [1,0,1,2,1,3,1,1,4] = Green face
  [2,4,4,2,2,5,1,4,2] = Orange face
  [2,2,5,3,5,3,2,0,5] = White face
  
  ```
  The order of represented faces is the same as the one of colors.
- ### How to represent your scrambled cube
  - First, take the blue face in front of you with the **yellow face up**.
  - Then, you need to represenet the yellow face by using the number above by beginning by the color in the top left corner.
  - Then, write the one to its right.
  - Then the one to its right again.
  - Now repeat this step with the row below.
  - And again with the row below.
  - You should now have the yellow face represented by numbers, and format it like this:
  ```
  
  3,0,5,5,0,5,0,4,0 or 3, 0, 5, 5, 0, 5, 0, 4, 0
  
  ```
  - **The order should be the order you red and wrote them before!**
  - Then do this exact same process for the blue face still with the **yellow face up**.
  - Then with the red face and **yellow face up**.
  - Then with the green face and **yellow face up**.
  - Then with the orange face and **yellow face up**.
  - Then with the **white face and _blue face up_**.
  - You should now have the representation of the 6 faces, you just have to concatenate them and put them between '[ ]', it should look like this:
  ```

  [3,0,5,5,0,5,0,4,0,3,2,4,1,3,4,3,1,0,0,3,4,1,4,5,3,0,5,1,0,1,2,1,3,1,1,4,2,4,4,2,2,5,1,4,2,2,2,5,3,5,3,2,0,5]

  ```
  - You can now copy/paste it when the program is asking for your representation.
  - The program should print you the solution.
  - #### Remember, you should apply the solution given with the blue face in front and yellow face up!
  
## Comment utiliser le programme

Pour l'utiliser, lancez useSolver.py, il vous sera demandé une représentation de votre cube, voilà comment le systeme marche :

Un Rubik's Cube est représenté dans notre code par un tableau de dimension 1 comportant 54 entiers de cette façon (c'est seulement un exemple !) :
```

[3,0,5,5,0,5,0,4,0,3,2,4,1,3,4,3,1,0,0,3,4,1,4,5,3,0,5,1,0,1,2,1,3,1,1,4,2,4,4,2,2,5,1,4,2,2,2,5,3,5,3,2,0,5]

```
Ils représentent chacun une couleur du cube.
Vous allez avoir besoin de ce tableau pour que le programme puisse résoudre votre cube, voici comme l'obtenir :
- ### Représentation des couleurs :
  Chaque couleur est assignée à un nombre :
  
  - Jaune = 0
  - Bleu = 1
  - Rouge = 2
  - Vert = 3
  - Orange = 4
  - Blanc = 5
  
  L'ordre n'est pas aléatoire et est lié à la représentation sous forme de tableau.
- ### Représentations et ordre des faces
  La représentation est composée de 6 représentations individuelles des 6 faces du Rubik's Cube, ce qui donne avec l'exemple précédent :
  ```
  
  [3,0,5,5,0,5,0,4,0] = Face jaune
  [3,2,4,1,3,4,3,1,0] = Face bleue
  [0,3,4,1,4,5,3,0,5] = Face rouge
  [1,0,1,2,1,3,1,1,4] = Face verte
  [2,4,4,2,2,5,1,4,2] = Face orange
  [2,2,5,3,5,3,2,0,5] = Face blanche
  
  ```
  L'ordre des faces représentées est le même que celui des couleurs.
- ### Comment représenter votre cube mélangé
  - Premièrement, prenez la face bleu devant vous avec la **face jaune au-dessus**.
  - Ensuite, vous allez représentez la face jaune avec les nombres au-dessus en commençant par la couleur en haut à gauche.
  - Ensuite, écrivez celle à sa droite.
  - Ensuite, celle à la droite de la précendente.
  - Maintenant, répetez cette étape sur la ligne du dessous.
  - Et encore avec la ligne du dessous.
  - Vous devriez maintenant avoir la représentation de la face jaune, ecrivez là ainsi :
  ```
  
  3,0,5,5,0,5,0,4,0 ou 3, 0, 5, 5, 0, 5, 0, 4, 0
  
  ```
  - **L'ordre doit être celui avec lequel vous avez lu et écrit les couleurs**.
  - Ensuite, répétez ce procédé pour la face bleue, toujours avec la **face jaune au-dessus**.
  - Ensuite pour la face rouge avc la **face jaune au-dessus**.
  - Ensuite pour la face verte avec la **face jaune au-dessus**
  - Ensuite pour la face orange avec la **face jaune au-dessus**
  - Ensuite pour la **face blanche devant avec la _face bleue au-dessus_**.
  - Vous devriez maintenant avoir les représentations des 6 faces, vous devez juste les concaténer et les mettre entre '[ ]', cela devrait ressembler à cela :
  ```

  [3,0,5,5,0,5,0,4,0,3,2,4,1,3,4,3,1,0,0,3,4,1,4,5,3,0,5,1,0,1,2,1,3,1,1,4,2,4,4,2,2,5,1,4,2,2,2,5,3,5,3,2,0,5]

  ```
  - Vous pouvez maintenant la copier-coller quand le programme vous la demande.
  - Le programme vous donnne alors la résolution.
  - #### Attention, vous devez appliquer les mouvements de résolution avec la face bleue devant et la face jaune au-dessus.

**Les explications en français sont en-dessous.**

## How does our algorithm work ?

Our first idea was to solve the cube as it's done in blind speedcubing because we wouldn't have to code movemements to change the representation of the cube in the code. We only needed a representation of the scrambled cube and we could solve it. We coded this with the basic Pochmann method but it was very slow (~ 300 moves to solve the cube), so we started searching for faster blind methods. We learned about the [Beyer-Hardwick method](https://www.speedsolving.com/wiki/index.php/Beyer-Hardwick_Method) to solve the edges. It was really fast, so we decided to use it. Then Lucas had the brilliant idea that we have an advantage over blind speedsolvers: we can modify the representation of the cube in our 'head'(program). So we needed the fastest way to solve corners, he then had another brilliant idea, solving the corner of a 3x3x3 cube is like solving a 2x2x2 cube! So we choosed to use the [Ortega method](https://www.speedsolving.com/wiki/index.php/Ortega_Method) to solve corners. That's the main idea of our algorithm, here is some more in depth explanation.

### First part : solving corners

As we explained, we solve corners using the Ortega method. The principle is to get all white corners on the white face, all yellow corners on the yellow face then, you only have 5 cases to solve corners.

- We choosed to place white corners first.
- We first check if there is any corners already well placed.
- Then, while all white corners are not well placed:
  - We check if the Yellow-Green-Orange corner has white.
  - If it's the case, we look where there is place to put the corner on the white face.
  - We do the coresponding move to place the corner on the white face with the white sticker of the corner facing the wite face.
  - If it's not the case, we check another corner until we find one and repeat previous steps.
- When all white corners are on the white face, all yellow corners now are on the yellow face.
- We now need to align corners(make yellow sticker of the corner facing the yellow face of the cube)
- The Orthega method gives us method to do this (it's like [OLL](https://www.speedsolving.com/wiki/index.php/OLL) but without placing edges so the algorithm are shorter). So we detect the case by looking at where are placed yellow stickers of corners and apply the corresponding algorithm.
- We then look at colors of corners to know in which case of the Orthega method we are.
- We apply the corresponding algorithm.

Corners are now solved!
