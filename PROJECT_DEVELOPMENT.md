# 10SE6A Assessment Task 2 - Project Development

## Data Selection & Game Attributes
For the specifications for each car, I've chosen to use the ANCAP safety rating, top speed, engine size, fuel economy, power to weight ratio, and range.

|Specifications     |Units        |
|-------------------|-------------|
|Top Speed          |km/h         |
|Range              |km           |
|Engine Size        |L            |
|Fuel Economy       |L/100km      |
|Power-To-Weight    |kW/t         |
|ANCAP Safety Rating|stars        |

An example of this would be:

|2025 Suzuki Swift Hybrid GLX Auto| |
|-------------------|-------------|
|Top Speed          |170          |
|Range              |750          |
|Engine Size        |1.2          |
|Fuel Economy       |4.6          |
|Power-To-Weight    |65.7         |
|ANCAP Safety Rating|1            |

From most powerful to least powerful, the attributes would go Power-To-Weight ratio, Fuel Economy, Range, Engine Size, ANCAP Safety Rating, and then Top Speed.   

For each of the attributes, I had different reasons for choosing them.
- I chose Power-To-Weight ratio because whilst Top Speed is a factor that would be great for a Top Trumps style card game, the Power-To-Weight ratio takes weight into account, so 2 cars with the same Top Speed would have a different Power-To-Weight ratio, the lighter one will have the better Power-To-Weight ratio. This is a fair attribute in gameplay, as 2 cards that would otherwise be alike will be more accurately seperated based on which one is stronger.
- I chose Fuel Economy because a car with a better fuel economy will run better than a car with a larger engine size. This could potentially be unfair though, as a car that is much worse overall may still have a better fuel economy, even if it has a significantly lower top speed, engine size and range.
- I chose to use the Range, as a car with a better range would be better than a car with a better top spped, as you can go further in a car with a higher range, even if another car would be quicker. This is fair in gameplay, as all cars will have a certain range affected by their fuel economy and engine size that is an accurate representation of how powerful the car is.
- I used Engine Size, as a car that can hold more fuel will typically have a better range than other cars. However, this could be unfair in gameplay as a car could have a large Engine Size but still be significantly worse in other aspects.
- The ANCAP Safety Rating was selected, as safety is a key feature of cars that is often overlooked. However, this is an unfair attribute as it can only be rated from 1-5, so 2 virtually different cars can have the same ANCAP Saftey Rating.
- Top Speed is the final attribute selected, as faster cars tend to be valued more. This is unfair though, as a car with a higher top speed might not be as efficient or have as good of a range as other cars.

These attributes together though are mostly fair, as they are found in all cars, so every car has a fair chance of winning. If I'd selected attributes only found in certain types of cars, like supercars or hybrids, this would be unfair to every other car that would normally be quite powerful.

## Class Design
The game will require 5 different classes - the Car, Card, Deck, Player & Game. The following table details the attributes and methods of the class alongside the role the class will play in the overall system

|Class |Attributes |Methods |Role |
|------|-----------|--------|-----|
|Car   |<ul><li>Top Speed</li><li>Range</li><li>Engine Size</li><li>Fuel Economy</li><li>Power-To-Weight Ratio</li><li>ANCAP Safety Rating</li></ul>|N/A|Contains all the attributes that each individual Card will contain|
|Card  |N/A|<ul><li>Display Car Data</li></ul>|Holds the data of it's car. It makes up the deck and is what the player uses to try to win|
|Deck  |N/A|<ul><li>Shuffle Deck</li><li>Deal Card</li></ul>|Made up of up to 30 cards. Its job is to shuffle the cards and deal them to the players|
|Player|<ul><li>Name</li><li>Hand</li><li>Score</li></ul>|<ul><li>Select Attribute</li><li>Play Card</li><li>Receive Card</li></ul>|Each player in the game. Holds cards and selects the attributes to be compared|
|Game  |<ul><li>Rounds</li></ul>|<ul><li>Start Game</li><li>Play Round</li><li>Compare Cards</li><li>Choose Winner</li><li>Manage Draw</li><li>End Game</li></ul>|Main game loop that handles playing the game, how many rounds there are, and determining who wins|

## Class Diagram

![Class diagram explaining the relationship of each class](/Images/ClassDiagram.png "UML Class Diagram") 

## Game Mechanics Design
When the game begins, the number of rounds and players will be chosen. Afterwards, each player will get a certain amount of cards based on how many players there are. When the round begins, the first player will select an attribute to compare. Each player selects a card, and the values of all those cards is displayed, and whoever has the highest value wins the round and gets all the cards that were played. If 2 cards both have the same value, the cards of the other players will be placed back into the deck. The winner is the last one left when all the other players lose all their cards. The game will go on until a winner is determined.

![Structure chart](/Images/StructureChart.png "Structure Chart") 

## Interface & Card Design

![Template for what a card will look like](/Images/CardDesign.png "Card Design") 
![Sketch of how the game will look](/Images/InterfaceSketch.png "Interface Sketch") 

The game will show the players card to him, while the other players cards are hidden. When an attribute is selected and needs to be compared, a card will come up in the middle of the screen and all players cards will be revealed. Whichever player's card is the closest matching wins and gets that card added to their pile.

## Social, Ethical & Legal Implications
