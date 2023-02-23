# PlantUML

# Installing PlantUML in Jetbrains Tools

# Installing PlantUML Plugin

Open your Jetbrains IDE of choice (Webstorm, Pycharm etc) and open the Settings (CTRL+,) or under the File Menu.

Select the Plugins option in the left-hand side menu, and then the Marketplace tab.

![Screen Shot 2022-08-13 at 11.35.37 am.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/Screen_Shot_2022-08-13_at_11.35.37_am.png)

Search for PlantUML and click Install next to “PlantUML Integration”.

<aside>
‼️ If the button says “Installed” instead of “Install”, click Ok and ignore the rest of the instructions.

</aside>

![Screen Shot 2022-08-13 at 11.36.50 am.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/Screen_Shot_2022-08-13_at_11.36.50_am.png)

After a moment, the Install button will change to a Restart IDE button. Select that.

![Screen Shot 2022-08-13 at 11.38.29 am.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/Screen_Shot_2022-08-13_at_11.38.29_am.png)

Once your IDE has been restarted, the plugin is fully installed.

# Writing PlantUML Use Case Diagrams

## Start and End

To start a PlantUML diagram, the first line is to define the type of diagram you’re attempting to draw. In the case of a Use Case Diagram, the first line should be:

```
@startuml
```

The corresponding final line will be:

```
@enduml
```

The remainder of the code appears between those two lines.

![final.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/final.png)

## Actors

The next stage is to define the different actors in the system, using the keyword `actor` followed by the name to appear under the actor in the diagram, followed by the identifier. For example `actor "Unregistered User" as unregistered` creates a new actor, with the text “Unregistered User below the icon, and this will be identified later in the code as `unregistered`.

List all the actors that are required for the Use Case Diagram, directly after `@startuml`.

For example:

```
@startuml NgunnawalWebsite
left to right direction
actor "Unregistered User" as unregistered
actor Administrator as admin
actor "Registered User" as registered

@enduml
```

![NgunnawalWebsite3.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/NgunnawalWebsite3.png)

## Use Case Packages

Next define any groups of similar functionality of the system you’re implementing. For instance, you may group all the administrative functions together, and all the user functionality together. This is a design choice and many systems can be organised in different ways, so there is no 100% correct answer.

Define the packages with the `package` keyword and the package name. Place these after the actors definitions.

For example:

```
@startuml NgunnawalWebsite
left to right direction
actor "Unregistered User" as unregistered
actor Administrator as admin
actor "Registered User" as registered

package NgunnawalWebsite {
 
}

@enduml
```

![NgunnawalWebsite4.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/NgunnawalWebsite4.png)

## Use Cases

Inside each package, indicate the functionality provided by the system. This is done inside each package, using the `usecase` keyword followed by the text displayed in the diagram and an identifier.

For example. This use case will display in the diagram as “User Registration” and can be referred to later as UC1.

```
package NgunnawalWebsite {
 usecase "User Registration" as UC1
}
```

![NgunnawalWebsite2.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/NgunnawalWebsite2.png)

## Link Actors to Use Cases

The final step is to link Actors and Use Cases. This is where the diagram ties everything together, showing which actors can access which use cases, which is the point of the diagram.

After packages have been declared, connect the actors to the use cases,  *using their identifiers*.

For example:

```
unregistered --> UC1
```

![NgunnawalWebsite1.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/NgunnawalWebsite1.png)

You can also add labels to the links by using the following format:

```
unregistered --> UC1 : Only needed once.
```

![NgunnawalWebsite.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/NgunnawalWebsite.png)

# Create a PlantUML File

Inside your Project, right click on the project name and choose New → PlantUML file.

![Screen Shot 2022-08-13 at 2.22.09 pm.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/Screen_Shot_2022-08-13_at_2.22.09_pm.png)

Give the file a name and choose the type of diagram you’re creating.

![Screen Shot 2022-08-13 at 2.24.22 pm.png](PlantUML%20473ebd6014794691a492d2efef4fcfe9/Screen_Shot_2022-08-13_at_2.24.22_pm.png)

An example UML diagram is included when a file is created. This code can be deleted, or modified depending on your needs.

# PlantUML Introduction

# PlantUML Introduction

> **PlantUML** is an open-source tool allowing users to create diagrams from a plain text language
[https://en.wikipedia.org/wiki/PlantUML](https://en.wikipedia.org/wiki/PlantUML)
>