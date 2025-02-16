Great! Let's start from **C# Fundamentals**, since it's the foundation of everything in 2D game development.  

---

# **Lesson 1: Variables, Data Types, and Operators in C#**

### **🔹 What Are Variables?**
A **variable** is a container that holds data. In C#, every variable has a **type** that determines what kind of data it can store.

### **🔹 Declaring and Initializing Variables**
In C#, you must declare a variable before using it. The syntax is:

```csharp
<data_type> variableName = value;
```

Example:
```csharp
int health = 100; // Integer variable storing health points
float speed = 5.5f; // Floating-point variable storing movement speed
string playerName = "Warrior"; // String variable storing player's name
bool isAlive = true; // Boolean variable storing true/false
```

---

## **1️⃣ Basic Data Types in C#**
C# has several data types. The most common ones used in game development are:

| Data Type  | Example Value | Purpose in Game Dev |
|------------|--------------|----------------------|
| `int` | 100 | Used for whole numbers (Health, Score, Ammo count) |
| `float` | 3.5f | Used for precise numbers (Speed, Gravity, Position) |
| `double` | 99.99 | More precision than `float` |
| `bool` | true / false | Used for conditions (Is player alive?) |
| `char` | 'A' | Stores a single character |
| `string` | "Player1" | Stores text (Player name, Game messages) |

### **🔸 Example of Different Data Types in a Game**
```csharp
int score = 0;          // Keeps track of the player's score
float jumpHeight = 2.5f; // How high the player can jump
bool hasKey = false;    // Does the player have the key?
string levelName = "Dungeon"; // Name of the current level
```

---

## **2️⃣ Operators in C#**
Operators allow us to perform operations on variables.

### **🔹 Arithmetic Operators**
Used for basic mathematical operations:

| Operator | Meaning | Example |
|----------|---------|---------|
| `+` | Addition | `score = score + 10;` |
| `-` | Subtraction | `health = health - 20;` |
| `*` | Multiplication | `damage = attackPower * 2;` |
| `/` | Division | `speed = maxSpeed / 2;` |
| `%` | Modulus (Remainder) | `coins = 10 % 3;` (Result: 1) |

**Example in Game Dev:**
```csharp
int playerHealth = 100;
int damage = 25;
playerHealth = playerHealth - damage; // Health reduces by 25
Console.WriteLine("Player Health: " + playerHealth);
```

---

### **🔹 Comparison Operators**
Used for making decisions (often in `if` conditions):

| Operator | Meaning | Example |
|----------|---------|---------|
| `==` | Equal to | `if (score == 100) { Win(); }` |
| `!=` | Not equal to | `if (lives != 0) { Play(); }` |
| `>` | Greater than | `if (speed > 10) { Boost(); }` |
| `<` | Less than | `if (health < 20) { Heal(); }` |
| `>=` | Greater than or equal to | `if (coins >= 100) { BuyItem(); }` |
| `<=` | Less than or equal to | `if (ammo <= 5) { Reload(); }` |

**Example in Game Dev:**
```csharp
if (playerHealth <= 0) 
{
    Console.WriteLine("Game Over!");
}
```

---

### **🔹 Logical Operators**
Used for combining multiple conditions:

| Operator | Meaning | Example |
|----------|---------|---------|
| `&&` | AND | `if (health > 0 && hasKey) { OpenDoor(); }` |
| `||` | OR | `if (ammo > 0 || meleeWeapon) { Attack(); }` |
| `!` | NOT | `if (!isAlive) { Respawn(); }` |

**Example in Game Dev:**
```csharp
bool hasKey = true;
bool doorUnlocked = false;

if (hasKey && !doorUnlocked) 
{
    Console.WriteLine("You unlocked the door!");
}
```

---

## **3️⃣ Constants and Variables Scope**
### **🔹 Constants (`const`)**
A **constant** is a variable whose value **never changes**.

Example:
```csharp
const float gravity = 9.8f; // Gravity value in the game, never changes
```

### **🔹 Scope of Variables**
- **Local Variables** – Exist inside methods and functions.
- **Global Variables** – Exist throughout the entire class.

Example:
```csharp
class Player
{
    int health = 100; // Global variable

    void TakeDamage()
    {
        int damage = 20; // Local variable
        health -= damage;
    }
}
```

---

## **4️⃣ Hands-on Mini Game Concept**
### **🔹 Task:** Create a simple **Health System** in C#
**Try implementing this yourself:**
```csharp
using System;

class Game
{
    static void Main()
    {
        int playerHealth = 100;
        int damage = 20;

        Console.WriteLine("Player takes damage!");
        playerHealth -= damage;

        Console.WriteLine("Player Health: " + playerHealth);
    }
}
```

---

## **🎯 What You Learned in This Lesson**
✔ What variables are and how to declare them  
✔ Different data types used in game development  
✔ Operators and how they work in C#  
✔ Scope of variables and constants  
✔ A simple **health system** example  

---

## **Next Lesson: Control Flow (if-else, switch-case, loops)**
This will help in making **decisions** in games (e.g., "If health is 0, show Game Over screen"). Ready? 🚀