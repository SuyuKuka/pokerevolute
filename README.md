# Pokerevolute

## About

**Pokerevolute** is a Java-based Tower Defense game developed as a second-year Bachelor's (L2 Informatique) project at Université Paris Cité. Built entirely from scratch, this project demonstrates a strong command of advanced Java concepts, including object-oriented design patterns, MVC architecture, custom graphical rendering with Java Swing, and event management.

The game combines traditional tower defense mechanics with the Pokémon universe, featuring unique towers with experience progression, evolutions, dual damage types, active skill management, and dynamic hero buffs.

*Note: As this was originally an academic project evaluated on architectural design, the codebase emphasizes modular separation between core game logic (`model`), user inputs (`control`), and graphical views (`graphics`). The source code and comments may contain some French. The interface is fully in French.*

## Tech Stack

- **Language:** Java
- **UI & Graphics:** Java Swing, Custom 2D Graphics & GIFs
- **Data Management:** CSV loaders for configurations and Pokémon stats
- **Audio:** WAV sound effects and background tracks
- **Build System / Tools:** Java JAR / IDE compilation

## Key Features

- **Unique Pokémon Towers:** Each tower is unique (limited to one instance on the field), featuring custom levels, experience progression, evolutions, and up to 4 swappable skills.
- **Dual Damage & Type Systems:** Incorporates physical and special damage types, alongside a comprehensive type-advantage matrix (e.g., Fire is strong against Grass but weak against Water).
- **Dynamic Heroes:** Choose a hero before starting (such as Sacha, Ondine, Pierre, Max, or Team Rocket), each granting specific passive bonuses to towers or debuffs to enemies.
- **Multiple Game Modes:** 
  - *Classic Mode:* Defeat a set number of waves depending on difficulty to earn player experience.
  - *Marathon Mode:* Endless waves with escalating difficulty.
- **PC Management System:** Access a PC interface before starting a game and every 6 waves to reorganize your active team of up to 6 towers.
- **Procedural Maps & Seasonal Themes:** Randomly generated maps with seasonal visual variants (Spring, Summer, Autumn, Winter).
- **Dual Interface Support:** Fully functional graphical interface (GUI) as well as an alternative terminal-based execution mode.

## Project Structure

```text
📁 pokerevolute
│
├── 📁 docs/
│   ├── 📄 DIAGRAM.png              # Project architecture diagram
│   ├── 📄 Rapport.pdf              # Detailed academic project report (in French)
│   └── 📄 Source.txt               # Asset sources and attributions
│   
├── 📁 ressources/                  # Game assets
│   ├── 📁 background/              # Background images and banners
│   ├── 📁 button/                  # UI buttons and interactive states
│   ├── 📁 config/                  # CSV configuration and data files
│   ├── 📁 heroprofile/             # Hero avatars and portraits
│   ├── 📁 music/                   # Battle and main menu soundtracks (.wav)
│   ├── 📁 profile/                 # User profile layouts
│   ├── 📁 projectiles/             # Attack animations and projectiles per type
│   ├── 📁 sprite/                  # Pokémon animated sprites (GIFs)
│   ├── 📁 team/                    # Team management UI elements
│   ├── 📁 tiles/                   # Seasonal map tiles (Spring, Summer, Autumn, Winter)
│   └── 📁 type/                    # Type badge icons (Fire, Water, Plant, etc.)
│
├── 📁 src/                         # Java source code (.java)
│   ├── 📁 characters/              # Specific Pokémon implementations & Starters
│   ├── 📁 control/                 # Game controllers & terminal handling
│   ├── 📁 graphics/                # Swing views, screens, menus, and project-specific GUI
│   ├── 📁 main/                    # Main game entry point
│   └── 📁 model/                   # Core logic (Towers, Enemies, Waves, Maps, Types)
│
├── 📄 README.md                    # Project documentation
└── 📄 pooproject.jar               # Pre-packaged executable JAR
```

## Getting Started

### Prerequisites

* Java Development Kit (JDK).

### Installation & Execution

1. Clone the repository:
```bash
git clone https://github.com/SuyuKuka/pokerevolute.git
cd boards-adventure
```

2. Launch the Game:  
    * Windows: Double-click the provided `run-game.bat` script.
    * Linux / macOS / Other Systems: Run the application directly via command line:

* Graphical Mode: 
```bash
java -jar pokerevolute.jar
```
* Terminal Mode:
```bash
java -jar pooproject.jar [termccinal]
```

### Compiling and Running Manually (Without JAR)

If you prefer to compile the source code yourself:
1. **Compile the Java files:**
```bash
javac -d bin ./src/main/*.java ./src/model/*.java ./src/graphics/*.java ./src/control/*.java ./src/characters/*.java
```

2. Execute the Graphical Mode:
```bash
java -cp bin main.Game
```

3. Execute the Terminal Mode:
```bash
java -cp bin main.Game [termccinal]
```

## Controls & Navigation

*Note: The game may uncounter unexpected behavior or crashes. And is also not balanced to win at all.*

Mouse Left Clicks: Used extensively across the main menu, tower placement, inventory PC management, and button interactions (speed up, pause, etc.).  
Mouse Right Clicks: Used to remove tower information after left clicked on it.  
Mouse Hover: Hover on the enemy on the left to see details about them on bottom left.  

## Team

This project was developed collaboratively as a 2-person team:

- **CHEN Michel** - Java Development & Game Architecture 
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/SuyuKuka)
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?logo=linkedin)](https://linkedin.com/in/chen-michel)

- **LIU Kai-Xiang** - Java Development & Game Architecture 
  [![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?logo=github)](https://github.com/Peak4s)

## License

This project was developed for academic purposes at **Université Paris Cité** and is provided for portfolio demonstration purposes. 

**Code:** The source code of this project is open-source and available under the GPL 3.0 License — see [LICENSE](LICENSE) for details.

**Assets:** Images assets (such as icons, etc) belong to their respective copyright owners. They are included here strictly for educational and portfolio demonstration purposes and are not distributed under an open-source license. Asset sources and credits are detailed in Source.txt.
