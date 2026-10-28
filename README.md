# Cosmic Escape

**Team 14 | CMPT 276, Fall 2025 | Simon Fraser University**

A 2D top-down arcade game built in Java with the [LITIengine](https://litiengine.com/) game engine, featuring power-ups, hazards, and enemies with line-of-sight vision.

**Play it:** [michaelgdev.itch.io/cosmic-escape](https://michaelgdev.itch.io/cosmic-escape)
**Game Demo:** https://youtu.be/d250ylmZjH8

> **Code-only repository.** This is a public, source-only copy of our team's course repository. The art, music, sound effects, fonts, and the LITIengine resource file (`cosmic-escape.litidata`, which bundles the sprites and sounds) have been removed because they are third-party assets that are not licensed for redistribution. Generated build output and Javadocs were removed as well. Commit history, authors, and dates are preserved.
>
> Because the assets are missing, the game will not run from this source as-is, and tests that load game assets will fail. To play the game, use the itch.io link above.

## Team

| Member | Role / Contributions |
|---|---|
| **Michael Gonzales** | Managed team tasks, milestones, and code reviews; implemented core gameplay, including trigonometry-based collision handling and projected enemy sight lines; refactored rendering and interaction code into reusable classes; wrote JUnit tests |
| Jugraj Tatla | |
| Praneet Kaur Bhasin | Implemented core gameplay features; refactored rendering and interaction code into reusable classes; wrote JUnit tests |
| Zihan Wang | |
| Palash Dalsaniya | Implemented power-ups; wrote and maintained tests |

## Highlights

- Voted "Best Game" in a class-wide peer vote
- 84% line and 60% branch test coverage (JUnit 5, JaCoCo)
- Javadocs and a runnable JAR generated with Maven
- Built and managed with Maven

## Project Structure

```
src/main/java/ca/sfu/cmpt276/fall2025/team14/
  app/       entry point and core game logic
  model/     player, enemies, power-ups, hazards, and animation controllers
  screens/   main menu, in-game screen, HUD, and win screen
  utils/     map object loaders, path following, and vision helpers
src/main/resources/maps/   level layouts (Tiled .tmx/.tsx)
src/test/java/...          unit and integration tests
```

## Prerequisites

- **Java Development Kit (JDK):** version 25 (as specified in `pom.xml`) or a compatible version
- **Apache Maven**

## Building the Project

From the project root, run:

```
mvn clean
mvn compile
mvn package
```

This cleans previous builds, compiles the code, and packages it into a JAR file in `target/`.

## Testing

The project uses JUnit 5. To run the tests and generate a JaCoCo coverage report:

```
mvn clean test
mvn jacoco:report
```

The coverage report is written to `target/site/jacoco/index.html`. Tests that depend on the removed assets will fail in this repository.

## Documentation (Javadocs)

To generate the HTML documentation from the source comments:

```
mvn javadoc:javadoc
```

Then open `target/reports/apidocs/index.html` in any web browser.

## Credits

The original game uses the following assets. They are **not included** in this repository.

- **Engine:** [LITIengine](https://litiengine.com/)
- **UI art:** [Complete UI Essential Pack](https://crusenho.itch.io/complete-ui-essential-pack) by Crusenho, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
- **Sprites and tiles:** [Tech Dungeon: Roguelite](https://trevor-pupkin.itch.io/tech-dungeon-roguelite) by Trevor Pupkin
- **Font:** monogram by datagoblin
- **Music and sound effects:** royalty-free tracks from [Pixabay](https://pixabay.com/)
