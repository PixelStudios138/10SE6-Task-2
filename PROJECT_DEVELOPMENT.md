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
- I chose to use the Range, as a car with a better range would be better than a car with a better top spped, as you can go further in a car with a higher range, even if another car would be quicker. This is fair in gameplay, as
- I used Engine Size, as a car that can hold more fuel will typically have a better range than other cars. However, this could be unfair in gameplay as a car could have a large Engine Size but still be significantly worse in other aspects.
- The ANCAP Safety Rating was selected, as safety is a key feature of cars that is often overlooked. However, this is an unfair attribute as it can only be rated from 1-5, so 2 virtually different cars can have the same ANCAP Saftey Rating.

## Class Design

## Class Diagram

## Game Mechanics Design

## Interface & Card Design

## Social, Ethical & Legal Implications
