# **Unity Standards**

## **Code**

Public variables should not be used often. Use `[SerializeField]` to expose variables to the editor. 

Public properties and functions are ok. 

Use appropriate naming conventions.

Name each variable and function with a descriptive name.

If a script has gotten to be very long, consider creating additional scripts/components to break up the code.

Pay attention to code in update, `GetComponent`, `FindComponent` and loops in Update can be very inefficient. 

Remember to pay attention to the big picture. Map out scripts and systems before coding to reduce potential issues.

## **Namespaces** [[Documentation](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/namespaces)]
Namespaces are a great way to help organize code. For example, all scripts related to how the player works in a game could be in the player namespace. 

Namespaces allow scripts to have the same name as long as they are in a different namespace, which can reduce name length. 

## **Comments**

Comment code. This does not mean every line, but gives a broad description that allows a high level understanding of what is going on for others. 

Use  the `///` over functions, describing the function and its parameters. This xml commenting gives valuable intellisense to the function that can be read while hovering over it. 

## **Folder Structure**

Place assets in appropriate folders. Materials should be in a Materials folder, scripts in Scripts etc. Having an organized unity project folder structure will make asset finding easier for other members of the team. 

Putting scripts into sub-folders and organizing them by function makes finding them easier. 

## **Naming Conventions**

Name everything consistently, optionally using prefixes for specific types of assets. Teams can create and follow their own naming conventions.

### Example naming conventions (Files):

Material : Mat\_Name

Texture: Tex\_Name

Script: [DoSomething.cs](http://DoSomething.cs)

### Example naming conventions (code):

Public Variable: `SomeName`

Private Variable: `_someName`

SerializeField/Protected: `someName`

## **Prefabs \[[Documentation](https://docs.unity3d.com/Manual/Prefabs.html)\]** 

Work in prefabs when possible. Using prefabs will reduce changes to a scene and in turn will make merge conflicts less prominent. 

When updating prefabs within a scene, make sure to apply changes to the prefab if you wish for edits to persist to the prefab. 

## **Scriptable Objects \[[Documentation](https://docs.unity3d.com/6000.2/Documentation/Manual/class-ScriptableObject.html)\]** 
Scriptable Objects can be a useful tool for many different systems with development, most often used to store data. 

## **Test Scenes**

Each developer should have a folder with their own test scenes (some teams have test scenes organized by sprint/feature instead). Once their feature works in the test environment, it can then be moved into the main scene(s). Make sure your branch is updated to the latest version of `Dev`/ `Main` before moving new objects/features into the main scene. 

## **Scene Organization**

Keep each scene tidy. Use empty gameobjects to hold related objects together, such as Canvases, Lights etc. This will reduce clutter of the scene and make it easier to find needed objects.


