+++

title = "Introduction to Pseudocode"

categories = ["Common"]

language= "English"

+++
A group of friends is visiting you this evening, and you want to offer them homemade Mediterranean Pesto Pizza. The problem is that you do not know how to prepare it. You search for the recipe online, and you find that it can be cooked in three steps. The recipe looks as follows:

> **Step 1**
> Preheat an oven to 175 °C.
>
> **Step 2** 
Spread pesto onto the crust; top with feta cheese, tomatoes, and olives.
>
> **Step 3**
> Bake in the preheated oven until cheese is melted, 6 to 8 minutes.

Congratulations, your pizza was a success; your friend loved it. **But what does a Mediterranean Pesto Pizza has to do with programming?**

In very simplistic terms, cooking is nothing more than following a series of instructions until a dish is produced. Likewise, a computer program is nothing more than a series of instructions (i.e., commands) that, once executed in a specific order, a result is obtained.

Chefs follow a **recipe** to create a dish. Likewise, developers follow an **algorithm** to create a software program.

# What is an Algorithm?
An *Algorithm* is a **sequence of instructions** on how to achieve a task.

Your role as a developer is simple: **For every problem you encounter, create an algorithm that solves it**. For example, let's say you have to develop a computer program that calculates the area of a triangle.

How would the algorithm be?

> ### Area of a Triangle Algorithm
> **Step 1**
> Get the base of the triangle
>
> **Step 2** 
> Get the height of the triangle
>
> **Step 3**
> Calculate the area by multiplying *base* * *height* * 0.5
>
> **Step 4**
> Display the result to the user

When the computer program executes those steps, the program will successfully return the area of a triangle.

# First solve it on paper
The human brain is very complex and very smart. If I tell you to prepare me a sandwich, I do not need to specify every step to prepare a sandwich. However, the computer is not that smart. If I want to create a software application that prepares a sandwich, **I must specify every single step in a very detailed manner**; otherwise, I might end up with no sandwich or, worse yet, a burned kitchen.

Part of this programme is to help you develop what we call *the programming mindset*, which is thinking of problems in a very detailed manner. Developing the *programming mindset* begins by understanding and practicing the concept of *First Solve it on paper*. That means, **before you start writing your first line of code, you must have the solution on paper. (Yes, literally on paper)**. 

For example, if you want to create a software application that prepares a sandwich, your instinct will begin to write code, **but don't**. Instead, **solve the problem on paper first**: structure your ideas, structure the algorithm, and define the correct sequence of steps. Solving the issue on paper will help you find problems with your algorithm, even before you write the first line of code, and will help you focus on one thing at a time: first on solving the problem and then translating your algorithm into code.

The algorithm you write on paper is formally known as *pseudocode*.

# What is Pseudocode?
*Pseudocode* is an informal, high-level description of an algorithm. The main characteristics are the following:
- It is intended to be read by humans and not by computers.
- There is no code when writing pseudocode
- Describe **what** needs to be done and **not how** it needs to be done.

{{% notice warning %}}
Since pseudocode is an essential part of the programme, any time you present a solution to the class or request help from the instructor, you must show your pseudocode.
{{% /notice %}}

# Pseudocode Syntax
There is no formal syntax or way of writing pseudocode. However, for this programme, we will follow this syntax:

- **INPUT**: Indicates a user inputs a value
- **OUTPUT**: Indicates an output will appear on the screen
- **WHILE**: An iteration that has a condition at the beginning
- **FOR**: A counting iteration
- **IF – THEN – ELSE:** a decision in which a choice is made

Instructions that occur inside a *selection* or *iteration* statement are indented.

{{% notice note %}}
As of this module, it is acceptable not to understand what the `WHILE` and `FOR` do. However, we will learn more about them in the coming modules. 
{{% /notice %}}

### Example 1
Write pseudocode to calculate the area of a circle and print the result.

{{<kotlin>}}
INPUT radius of the circle
Use the equation "PI * radius * radius" to calculate the area
OUTPUT area of the circle
{{</kotlin>}}

### Example 2
Write pseudocode that asks the user for his age. If the number is less than `18`, print the sentence `minor`; otherwise, print `adult.`

{{<kotlin>}}
INPUT age
IF age < 18 THEN
    OUTPUT "minor"
ELSE
    OUTPUT "adult"
{{</kotlin>}}

### Example 3
Write pseudocode to prints all odd numbers from `50` to `100.`
{{<kotlin>}}
FOR number is 50 to 100
    IF number is odd
        OUTPUT number
{{</kotlin>}}

# Flowchart
Another way of visualizing pseudocode is by using flowcharts. The shapes to use for each of the Pseudocode commands is the following:

{{< mermaid align="left">}}
graph TD
    B[\INPUT\]
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
    B([OUTPUT])
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
    B[/FOR\]
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
    B[/WHILE\]
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
    B{IF};
{{< /mermaid >}}

{{< mermaid align="left">}}
graph TD
    B[Step];
{{< /mermaid >}}

Below we illustrate how to the flowchart version from the pseudocode examples above.

### Flowchart 1
{{< mermaid align="left">}}
graph TD
    A((Start)) --> B[\Get the radius of the circle\];
    B --> C[Use the equation PI * radius * radius to calculate the area];
    C --> D([Print the area]);
    D --> E((End));
{{< /mermaid >}}

### Flowchart 2
{{< mermaid align="left">}}
graph TD
    A((Start)) --> B[\Get age of the user\];
    B --> C{is age < 18};
    C --> |Yes| D([print 'minor'])
    C --> |No| E([print 'adult'])
    D --> F((End))
    E --> F
{{< /mermaid >}}

### Flowchart 3
{{< mermaid align="left">}}
graph TD
    A((Start)) --> B[/number is 50 to 100\];
    B --> E((End))
    B --> C{is number odd?};
    C --> |Yes| D([print number])
    D --> B
{{< /mermaid >}}
