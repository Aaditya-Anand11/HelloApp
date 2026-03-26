# HelloApp

Hello App starts with Hello World, progresses to displaying a user name, then names from command-line args and standard input. It then manages names in a collection with list/remove options, refactors into methods and classes, adds persistence across runs, and finally displays names in banner format.

## Summary

Hello App Use Case begins with simple display of Hello World then goes on to display user name then to displaying the names from the command line arguments and then from standard input and then managing the names in a collection with options to list and remove names and then refactoring the code to separate concerns into different methods and classes and finally adding persistence to the name list across runs. The final use cases involve enhancing the display of names by showing them in banner format.

## Use Case Roadmap

| UC | Branch | Description | Status |
|----|--------|-------------|--------|
| UC1 | `feature/UC1-display-hello` | Print a basic `Hello, World!` greeting | Done |
| UC2 | `feature/UC2-display-name` | Accept one name via command-line arg and greet | Done |
| UC3 | `feature/UC3-display-name-default` | Default to `World` if no argument provided | Done |
| UC4 | `feature/UC4-display-multiple-names` | Accept multiple names, display comma-separated | Done |
| UC5 | `feature/UC5-enhanced-for-loop` | Refactor UC4 using enhanced for-each loop | Done |
| UC6 | `feature/UC6-substring-method` | Use `substring()` to remove trailing delimiter | Done |
| UC7 | `feature/UC7-string-join` | Use `String.join()` for cleaner multi-name greeting | Done |
| UC8 | `feature/UC8-*` | Store entered names in memory and list them on request | Planned |
| UC9 | `feature/UC9-*` | Add removal support for stored names | Planned |
| UC10 | `feature/UC10-*` | Extract input-processing logic into dedicated methods | Planned |
| UC11 | `feature/UC11-*` | Move name-management responsibilities into a separate class | Planned |
| UC12 | `feature/UC12-*` | Persist names to storage and reload them across runs | Planned |

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
mvn exec:java -Dexec.mainClass="HelloApp"

# Run with a single name argument (UC2+)
mvn exec:java -Dexec.mainClass="HelloApp" -Dexec.args="Alice"

# Run with multiple names (UC4+)
mvn exec:java -Dexec.mainClass="HelloApp" -Dexec.args="Alice Bob Charlie"
```

## Example Output

```
# No arguments
Hello, World!

# Single argument: Alice
Hello, Alice!

# Multiple arguments: Alice Bob Charlie
Hello, Alice, Bob, Charlie!
```

## Branch Strategy

- `main` — stable, production-ready code
- `dev` — integration branch for all feature branches
- `feature/UC*` — individual use case implementation branches

## Author

Aaditya Anand
