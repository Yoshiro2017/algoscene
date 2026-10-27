# algoscene
Repository for Algobox scenes (in case if the Algobox servers go down).

## Overview
The `algoscene` project is a community-driven digital preservation repository specifically designed to safeguard, catalogue, and host Algobox scene files (`.phz`). Over time, central servers hosting community content for specialized simulation platforms, educational utilities, and sandbox software face risks such as service degradation, unexpected server outages, domain migrations, or permanent shutdowns. To mitigate these risks, `algoscene` acts as an independent mirror and long-term archive. By maintaining an offline-first, version-controlled library of scenes, the repository ensures that creators, researchers, and hobbyists maintain uninterrupted access to historical and contemporary scene data regardless of central server availability or network infrastructure status.

## Repository Structure
```plaintext
algoscene/
│
├── scenes/              # Central storage directory for all archived scene binary/data files
│   ├── 1001.phz         # Individual Algobox scene identified by its unique server key
│   ├── 1002.phz
│   └── ...
│
├── NAMES.md      # Master index mapping every unique numeric ID to its original scene title
│
└── README.md            # Comprehensive repository documentation and operational guidelines
```
The repository structure has been designed with minimalist principles in mind to facilitate efficient automated parsing, fast local search queries, and effortless mirroring across distributed Git nodes. All core files reside either at the root level or within dedicated single-tier subdirectories to maintain low directory depth and streamline scripting tasks.

## File Naming Conventions
To guarantee consistency, programmatic readability, and conflict-free version tracking, every file added to this repository must follow strict naming standardizations:

- **Scene Binary Files (`scenes/<scene_id>.phz`):**
  - All scene files must be placed directly inside the `scenes/` directory. Subdirectories within `scenes/` are strictly prohibited to maintain flat-structure simplicity.
  - Every scene file must be named exclusively after its official numeric or canonical alphanumeric identification number assigned by the original platform (e.g., `4092.phz`).
  - Filenames must be lowercase, contain no spaces or special symbols, and strictly preserve the standard .phz archive file extension.
  - Modifying the file name to include titles, author tags, or timestamps is prohibited, as metadata is managed separately to avoid breaking automated lookups.
- **Index Register (`NAMES.md`)**:
  - The `NAMES.md` file at the root level serves as the central metadata registry for the entire collection.
  - Each record inside the registry correlates a raw scene ID with its human-readable title, original author (if recorded), and description.
  - Formatting inside `NAMES.md` must maintain uniform line breaks and strict delimiter usage so that batch scripts and search tools can dynamically re-index the archive without encountering parse errors.
 
## Usage
Utilizing the `algoscene` archive involves a straightforward process for finding, acquiring, and running preserved scene files on your local installation:

**Cloning or Downloading the Repository:**
Begin by fetching the complete or sparse tree of the repository onto your local system using standard Git operations:
```bash
git clone https://github.com/username/algoscene.git
cd algoscene
```

**Searching for Specific Content:**
Because scene files are referenced strictly by ID numbers, open `NAMES.md` in any plain text editor or search through it via command-line utilities (such as `grep` on Linux/macOS or `Select-String` on Windows PowerShell) to locate the ID corresponding to your desired scene name.
```bash
grep -i "Simulation Name" "NAMES.md"
```

**Retrieving and Loading Files:**
Note the matching ID returned from your search (for example, 5081). Navigate to scenes/5081.phz. Copy or move this file into your local Algobox scenes working directory, then launch the Algodoo application and select the standard file open menu to load the scene.

## Contributing
Community contributions are vital to building a comprehensive and resilient archive. If you possess Algobox scene files that are not yet archived here, or if you hold metadata updates for existing files, please adhere to the following workflow:

1. Verify Uniqueness: Before submitting a pull request, check the existing repository tree and search `NAMES.md` to confirm that the scene ID does not already exist in the archive.
2. Prepare File Attachments: Confirm that your `.phz` file is uncorrupted, opens reliably in standard Algodoo environments, and uses its canonical ID as its primary file name.
3. Update the Index: Add a new line entry to `NAMES.md` matching the format of existing records. Ensure that line endings are saved using UTF-8 encoding to avoid file corruption.
4. Submit a Pull Request: Stage both the newly added `.phz` file in `scenes/` and the updated `NAMES.md` index file in a single commit, then issue a pull request titled with the relevant ID range and scene titles.
