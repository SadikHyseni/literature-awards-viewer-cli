# Literature Awards Viewer (Java 8)

A Java 8 console application, built in NetBeans, for exploring Nobel Prize in Literature winners from 1901 to 2022. It reads the data from `literature-prizes.txt` and lets you browse it through a text menu.

## Features

- Loads and parses `literature-prizes.txt` once at startup and keeps the data in memory
- Models the data with `LiteraturePrize` and `Laureate` classes
- Interactive console menu:

| Option | Action |
|--------|--------|
| `List` | Show every year a prize was awarded |
| `Select` | Show prize details for a chosen year |
| `Search` | Find laureates by name (partial match) |
| `Exit` | Close the program |

## Project Structure

```
literature-awards-viewer/
├── src/                    # Java source code
├── test/                   # Tests
├── nbproject/              # NetBeans project settings
├── build.xml               # Ant build script
├── manifest.mf             # JAR manifest
├── literature-prizes.txt   # Prize dataset (1901–2022)
└── LICENSE
```

## Dataset Format

Each year in `literature-prizes.txt` is a block ending with `-----`:

```
1904
Frédéric Mistral (1830-1914)|France|Provençal
"in recognition of the fresh originality and true inspiration of his poetic production..."
poetry, philology
José Echegaray (1832-1916)|Spain|Spanish
"in recognition of the numerous and brilliant compositions..."
drama
-----
```

- Line 1: year
- For each laureate:
  - `Name (birth-death)|Country|Language`
  - the prize citation in quotes
  - their genres, separated by commas

## Getting Started

### Requirements

- Java 8 (JDK) or later
- Apache Ant, or NetBeans

### Run in NetBeans

1. **File → Open Project** and select the folder.
2. Press **Run** (F6).

### Run from the command line

```bash
ant jar
java -jar dist/Task1.jar
```

Run it from the project root so the program can find `literature-prizes.txt`.

## License

MIT License. See [LICENSE](LICENSE).
