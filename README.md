# HelloApp

Hello App starts with Hello World, progresses to displaying a user name, then names from command-line args and standard input. It then manages names in a collection with list/remove options, refactors into methods and classes, adds persistence across runs, and finally displays names in banner format.

## Summary

Hello App Use Case begins with simple display of Hello World then goes on to display user name then to displaying the names from the command line arguments and then from standard input and then managing the names in a collection with options to list and remove names and then refactoring the code to separate concerns into different methods and classes and finally adding persistence to the name list across runs. The final use cases involve enhancing the display of names by showing them in banner format.

## Use Case Roadmap

| UC | Description |
|----|-------------|
| UC1 | Print a basic greeting in the console |
| UC2 | Accept one name via command-line input and greet that user |
| UC3 | Support optional argument handling with a default greeting path |
| UC4 | Handle multiple command-line names in one execution |
| UC5 | Read a single name from standard input (enhanced for loop) |
| UC6 | Read and process multiple names from standard input |
| UC7 | Store entered names in memory and list them on request |
| UC8 | Add removal support for stored names |
| UC9 | Extract input-processing logic into dedicated methods |
| UC10 | Move name-management responsibilities into a separate class |
| UC11 | Persist names to storage and reload them across runs |
| UC12 | Render greeting text in banner-style output for enhanced display |

## Project Structure

```
HelloApp/
├── pom.xml
├── .gitignore
├── README.md
├── docs/
│   └── HelloAppUC.md
└── src/
    ├── main/
    │   └── java/
    │       └── HelloApp.java
    └── test/
        └── java/
            └── HelloAppTest.java (optional)
```

## Prerequisites

- Java 17+
- Maven 3.6+

## Maven Commands to Compile and Run

```bash
# Compile the project
mvn compile

# Run with default greeting
mvn exec:java

# Run with a name argument
mvn exec:java -Dexec.mainClass="HelloApp" -Dexec.args="Alice"

# Run with multiple names (UC4+)
mvn exec:java -Dexec.mainClass="HelloApp" -Dexec.args="Alice Bob Charlie"
```

## Branch Strategy

- `main` — stable, production-ready code
- `dev` — integration branch for all feature branches
- `feature/UC*` — individual use case implementation branches

## Author

Aaditya Anand
