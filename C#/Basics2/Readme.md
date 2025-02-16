# **Lesson 2: Control Flow in C# (if-else, switch-case, loops)**  
Control flow determines how your program makes **decisions** and **repeats actions**, which is essential in game development.

---

# **1️⃣ Decision Making (if-else & switch-case)**  
Decision-making structures allow the game to respond dynamically to player actions.

## **🔹 if-else Statements**  
Used when you need to check **one or more conditions** and execute different code depending on the result.

### **📌 Syntax:**
```csharp
if (condition)
{
    // Code executes if condition is true
}
else
{
    // Code executes if condition is false
}
```

### **🎮 Example: Checking Player Health**
```csharp
int playerHealth = 50;

if (playerHealth <= 0)
{
    Console.WriteLine("Game Over!");
}
else
{
    Console.WriteLine("Keep fighting!");
}
```
✅ If `playerHealth` is **0 or less**, it prints `"Game Over!"`  
✅ Otherwise, it prints `"Keep fighting!"`

---

## **🔹 if-else-if Ladder**  
When there are **multiple conditions**.

### **🎮 Example: Enemy AI Behavior**
```csharp
int enemyHealth = 100;

if (enemyHealth > 75)
{
    Console.WriteLine("Enemy is aggressive!");
}
else if (enemyHealth > 30)
{
    Console.WriteLine("Enemy is defensive!");
}
else
{
    Console.WriteLine("Enemy is fleeing!");
}
```
✅ If health is **above 75**, the enemy is aggressive  
✅ If health is **between 30 and 75**, the enemy is defensive  
✅ If health is **30 or below**, the enemy flees  

---

## **🔹 switch-case Statement**  
A **switch statement** is used when you have **multiple options** and want cleaner code instead of multiple `if-else`.

### **📌 Syntax:**
```csharp
switch (variable)
{
    case value1:
        // Code executes if variable == value1
        break;
    case value2:
        // Code executes if variable == value2
        break;
    default:
        // Code executes if no match
        break;
}
```

### **🎮 Example: Player Weapon Selection**
```csharp
string weapon = "Sword";

switch (weapon)
{
    case "Sword":
        Console.WriteLine("You swing the sword!");
        break;
    case "Bow":
        Console.WriteLine("You shoot an arrow!");
        break;
    case "Magic":
        Console.WriteLine("You cast a spell!");
        break;
    default:
        Console.WriteLine("Unarmed! Find a weapon.");
        break;
}
```
✅ If the player chooses `"Sword"`, `"Bow"`, or `"Magic"`, the respective action occurs.  
✅ If they have no weapon, it prints `"Unarmed! Find a weapon."`  

---

# **2️⃣ Loops (Repeating Actions)**
Loops allow the game to execute the same **action multiple times**.

## **🔹 for Loop** (Fixed Repetitions)  
Used when you know **how many times** something should repeat.

### **📌 Syntax:**
```csharp
for (initialization; condition; update)
{
    // Code executes repeatedly
}
```

### **🎮 Example: Spawning Multiple Enemies**
```csharp
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine("Enemy " + i + " spawned!");
}
```
✅ This loop runs **5 times**, spawning 5 enemies.  
✅ `i++` increases `i` by 1 every time until `i <= 5` is false.  

---

## **🔹 while Loop** (Unknown Repetitions)  
Used when **you don’t know how many times** a condition will be true.

### **📌 Syntax:**
```csharp
while (condition)
{
    // Code executes repeatedly while condition is true
}
```

### **🎮 Example: Player Health Regeneration**
```csharp
int health = 20;
int maxHealth = 100;

while (health < maxHealth)
{
    health += 10;
    Console.WriteLine("Healing... Health: " + health);
}
```
✅ The player **regains health** in steps of 10 **until full**.  
✅ **Stops automatically** once health reaches **100**.  

---

## **🔹 do-while Loop** (Always Executes At Least Once)  
Similar to `while`, but **executes at least once**, even if the condition is false.

### **📌 Syntax:**
```csharp
do
{
    // Code executes once, then repeats while condition is true
} while (condition);
```

### **🎮 Example: Player Menu Display**
```csharp
string choice;

do
{
    Console.WriteLine("Choose an action: (Attack / Run)");
    choice = Console.ReadLine();
} while (choice != "Attack" && choice != "Run");

Console.WriteLine("You chose: " + choice);
```
✅ Ensures the player selects **a valid action**.  
✅ Even if they **enter an invalid choice**, the menu **keeps appearing**.  

---

# **3️⃣ Loop Control Statements**
These **modify loop behavior**.

## **🔹 break (Stop Loop Immediately)**
Stops the loop **entirely**.

### **🎮 Example: Stop Searching When Item Found**
```csharp
string[] inventory = { "Potion", "Shield", "Key", "Bow" };

foreach (string item in inventory)
{
    Console.WriteLine("Checking: " + item);

    if (item == "Key")
    {
        Console.WriteLine("Key found! Unlocking door...");
        break; // Stops checking further items
    }
}
```
✅ Stops checking once the **"Key"** is found.  

---

## **🔹 continue (Skip to Next Loop Cycle)**
Skips the **current loop iteration**, but **keeps looping**.

### **🎮 Example: Skipping Certain Enemies**
```csharp
for (int i = 1; i <= 5; i++)
{
    if (i == 3)
    {
        Console.WriteLine("Enemy 3 is hiding. Skipping...");
        continue; // Skip this enemy
    }

    Console.WriteLine("Enemy " + i + " attacks!");
}
```
✅ **Enemy 3 is skipped**, but other enemies attack normally.  

---

# **🎯 What You Learned in This Lesson**
✔ **if-else statements** for decision making  
✔ **switch-case** for choosing between multiple options  
✔ **for, while, and do-while loops** for repeating actions  
✔ **break and continue** to control loops  
✔ **Game-related examples** for each topic  

---

# **Next Lesson: Methods & Functions in C#**  
Functions allow us to organize **game logic into reusable blocks**, such as a `TakeDamage()` function or an `Attack()` function. Ready to continue? 🚀