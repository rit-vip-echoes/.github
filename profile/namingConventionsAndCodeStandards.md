# Naming Conventions

Generally, the most important thing when it comes to naming conventions is making sure naming conventions are consistent! They can vary across teams and projects, but as long as each team follows a consistent DOCUMENTED naming convention for their assets in a project then you should be fine. Try to keep names descriptive of what the file actually is; avoid names like `JackPederson1.cs, JackPederson2.cs` as that's not descriptive of the functionality of the script or file. 

Teams should all agree on a naming convention for their files early on in a project's development, and refresh the teams of the convention upon the start of a new semester so all the new files done by new team members are in line with the older files' naming convention and structure. 

# Coding Standards

Unity utilizes C# scripts, so we'll be following the largely agreed upon professional standards, which can be found [here](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions). I'll go through the main highlights that'll be most relevant to echoes, but I recommend you follow the link and read through yourself, especially if you wanna dig into the weeds of C#.

### Public Variables and the 'var' type

You should avoid declaring variables as public at all costs (properties and functions are fine). This exposes the data and breaks encapsulation, and is generally frowned upon. Instead, declare variables as private and then encapsulate them with a separate Property utilizing a getter and a setter.

An example of this may look like:

`private int myInt = 0;`

`public int MyInt { get {return myInt;} set {myInt = value;} }`

You can also choose to exclude a get or a set statement. For example, you may want a variable to be readable by other files but not settable, so you just include the get and exclude the set. 

One important thing not mentioned in the docs but that echoes follows is that we do not use the `var` variable type! Please declare your variables as `int`, `string`, `bool` etc., do not use var unless it is absolutely necessary! and even if it is, there's probably a better solution without it.

### Variable and Function Names

Variables and fields should all follow camelCase, i.e names should always start with a lowercase letter and every subsequent word start with uppercase, with all words joined together with no spaces.

An example of this would be `string myBeautifulWonderfulAwesomeCamelCaseString;`. Each new word starts with an uppercase letter, while the first word (my) starts lowercase.

On the other hand, functions, classes, and properties all should follow PascalCase. Similar to camelCase, except it starts with an uppercase letter.

An example would be `int void MyNewAwesomeFunction(int swag) {return (swag * 2);}`. In this example, the function is in PascalCase while the variables are in camelCase.

### Commenting

Please, please, please comment code. use `//` to write short one or two line comments describing a code section's functionality. You don't need to explain what the code itself does line by line, people should be able to get that from looking at the code. You want to use comments to help organize your code and allow people to find functionality easily.

Every function should have an XML comment above it. If you're using Visual Studio, then you can automatically generate the XML comment format by typing `///` above a function declaration.

Best practices is to generally avoid longer comments using `/* */`, as these longer comments could either be simplified into smaller comments or should be transferred to documentation rather than clog up lines and lines of code. 

All comments should begin with an uppercase letter and end with a period, with a single space between the `//` and actual comment itself. Comments should also be placed on their own separate line, not adjacent to code itself. 

### String Concatenation

Avoid using + to concatenate strings, instead use string interpolation, using `${}`. 

An example: 

`string a = "cheese ";`

`string b = "burger":`

`string cheeseBurger = $"{a},{b}";`

The string cheeseBurger would then be set to the string "cheese burger".

### Indentation

Probably not something people are going to care too much about on echoes, but proper indentation for C# is to use four spaces rather than pressing the tab key.


# Unity Conventions

### Prefabs
In the editor, you should try to utilize prefabs as much as possible. They allow for reusability between scenes and are good for avoiding merge conflicts. 

You can find more documentation on Prefabs [here](https://docs.unity3d.com/Manual/Prefabs.html).

### Namespaces 
Namespaces are a great way to help organize code. For example, all scripts related to how the player works in a game could be in the player namespace.

Namespaces allow scripts to have the same name as long as they are in a different namespace, which can reduce name length.

Documentation can be found [here](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/program-structure/namespaces).

### SerializeField
While you shouldn't use public variables, if you want to expose a variable to be changed in the editor you can write [SerializeField] before the access modifier. This allows you to edit a variable's value in editor, while still maintaining it as a private or protected variable.

### Scene Organization

Keep each scene tidy. Use empty game objects to hold related objects together, such as Canvases, Lights etc. This will reduce clutter of the scene and make it easier to find needed objects. Try to keep things in hierarchies to make scene organization efficient.


