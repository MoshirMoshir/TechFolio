---
layout: essay
type: essay
title: "Fabric, Patterns, and Code"
date: 2024-04-25
published: true
labels:
  - Software Engineering
  - Design Patterns
  - Learning
  - Reflection
---
## Design Patterns
In this short treatise, I will be going over what Design Patterns are, how they work, and why they're useful!


<img width="700px" class="rounded pe-4" src="../img/DesignPatterns/Fabric.jpg">
<br>

### Fabric
For this analogy to work, lets imagine code to be a piece of fabric. Some fabrics are simple, designed to be one color, no patterns, and meant to be used in a bigger project. Others, can have complex strings of wool woven into it, creating a rainbow of colors and multitude of patterns on the fabric; on it's own a centerpiece. Regardless, the way fabric is made is by repeatedly weaving together individual lines of wool, or another material, one after another until as a whole, they make up the fabric. In this way, Design Patterns similarly make up code; where while they may not necessarily be all the strings in a fabric, they may make up common implementations of certain designs, such as the way buttons are sewn on or the concept of plaid.

### Patterns
Take a look at the above image. At first glance, it may seems like a unique design. But at closer inspection, you begin to notice that it is actually made up of a multitude of repeated shapes. Though the shapes used may be the same, they are never really placed in a repeated order. This is similar to how Design Patterns function in code. Design Patterns act as concept of an algorithm, where common problems can be tackled by certain patterns of code that may be subject to change depending on the actual application.

### Code
One such example of a Design Pattern is the _Singleton_. This Design Pattern ensures that a class has only one instance and provides a public point of access to it. 
Here's a quick example of it in python:
```python
class Singleton:
    __instance = None   # Private variable to hold the instance
    
    @staticmethod       # Ensures that this method is constant for all instances of the Singleton
    def get_instance(): # If there's no Instance, creates one, otherwise, returns the existing Singleton
        if Singleton.__instance is None: 
            Singleton()
        return Singleton.__instance

    def __init__(self): # If a Singleton already exists, it returns it
        if Singleton.__instance is not None:
            raise Exception("This class is a Singleton!")
        else:
            Singleton.__instance = self

# Example:
var1 = Singleton.get_instance() # Assigns the Singleton to var1
var2 = Singleton.get_instance() # Assigns the Singleton to var2

print(var1 is var2) # Outputs True since var1 is referencing the same Singleton as var2
```

As you see, the actual Design Pattern of Singleton is more of a concept of the way a class's constructor and instance is established, but can be implemented in any class that needs it, regardless of the actual use-case of the class.

In my own code for a java text-based game, I have needed to create a class that tracks players and won't create a new instance of itself so the player's progress can be continually tracked throughout a play-session:

```java
public class PlayerManager {
    private static PlayerManager instance; // Private variable to hold a constant instance
    private List<Player> players;

    // Private constructor to prevent instantiation from outside
    private PlayerManager() {
          players = new ArrayList<>();
      }

    // Method to get the singleton instance
    public static PlayerManager getInstance() {
        if (instance == null) { // If instance doesn't exist, creates one
            instance = new PlayerManager();
        }
        return instance; // Otherwise, returns the existing one
    }
}
```

Just like the strings and fabric, Design Patterns are patterns that can make up code to satisfy certain desires of effects, using similar "Patterns" but can be made up of entirely different code, instance use-cases, and even coding languages!