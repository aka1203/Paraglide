<img width="1093" alt="LogoDarkReady" src="https://github.com/user-attachments/assets/d9c3df89-3937-4ba7-b278-c76bb44f14e9#gh-dark-mode-only"><br>
<img width="1093" alt="LogoLightReady" src="https://github.com/user-attachments/assets/7c2e239b-3684-436e-a23c-5ebf85db1ab9#gh-light-mode-only">

# Paraglide - Paragraph Processor

 A program designed to automate the process of **sequentially copying each paragraph** from a loaded .TXT file and moving to the **next paragraph upon detecting Ctrl[Cmd] + V input**.

## Overview

![Welcome](https://github.com/user-attachments/assets/26e3d119-6da2-4861-a337-dda5eeb73665)
![Comparison](https://github.com/user-attachments/assets/7a51a03d-a1bb-4598-aefa-8fd1ec112a88)
![Paste](https://github.com/user-attachments/assets/2d0b1ec6-81f7-4e3c-a32d-c3207a16cba8)
![Shortcut](https://github.com/user-attachments/assets/c40498b3-9945-4137-a20e-fec5a4978d1e)
![Sidebar](https://github.com/user-attachments/assets/2d5b2dab-b787-4ad0-b3da-d9ba4a2a7f2b)

## Key Features

 1. Load .TXT files and split paragraphs, displaying **previous/current/next** paragraphs.
 2. Monitor keyboard input and perform **actions based on key combinations**:
   - **Paste (Ctrl + V, Cmd + V)**: Copy the next paragraph.
   - **Shift + Arrow Keys (←→)**: Navigate to the previous/next paragraph.
     - **Shift + Alt (Opt) + Arrow Keys (←→)**: Navigate to the previous/next page.
   - **Shift + Arrow Keys (↑↓)**: Pause/Resume the program.
     - **Shift + Alt (Opt) + Arrow Key (↑)**: Toggle overlay.
 3. Process text based on **paragraph** or **line** depending on the style of the .TXT file.
 4. Display the **current paragraph in progress** with an overlay window and allow navigation between paragraphs.
 5. Save logs to restore the **last position** when reloading a previously processed file.
 6. Quickly **load previously worked files** within the app.

## Purpose of Development

 Inspired by [SB2Tool](https://github.com/JOWONRO/SB2Tool), this program addresses one major limitation of the original tool: **it was Windows-exclusive**. 

 Despite not being a professional coder, I enthusiastically leveraged GPT to create this program. Written in **JavaScript** (NPM, React, Electron), it works across platforms, making it **more versatile** than the Windows-only predecessor.

## Project Overview
```
📦 Paraglide
├── 📂 public                             # Static Resources
│   ├── 📂 icons                          # App Icons
│   └── 📂 UI_icons                       # UI Icons
│   
├── 📂 src                                # Source Code
│   ├── 📂 components                     # React Components
│   │   ├── 📂 Views                      # Main Component View Modes
│   │   │   ├── 📜 ListView.js            # List View
│   │   │   └── 📜 Overview.js            # Overview
│   │   ├── 📜 MainComponent.js           # Main Component
│   │   ├── 📜 OverlayComponent.js        # Overlay Component
│   │   ├── 📜 Settings.js                # Settings Component
│   │   └── 📜 Sidebar.js                 # Sidebar Component
│   │
│   ├── 📂 CSS # Stylesheets
│   │   ├── 📂 Controllers                # Global Styles for Settings Controllers
│   │   ├── 📂 Views                      # Main Component View Modes
│   │   │   ├── 📜 ListView.css           # List View Styles
│   │   │   └── 📜 Overview.css           # Overview Styles
│   │   ├── 📜 App.css                    # Global Styles
│   │   ├── 📜 MainComponent.css          # Main Component Styles
│   │   ├── 📜 OverlayComponent.css       # Overlay Styles
│   │   ├── 📜 Settings.css               # Settings Styles
│   │   └── 📜 Sidebar.css                # Sidebar Styles
│   │
│   ├── 📂 store                          # Redux Store
│   │   ├── 📂 slices                     # Redux Reducers
│   │   ├── 📂 utils                      # Processors
│   │   └── 📜 store.js                   # Redux Store Entry Point
│   │
│   ├── 📜 App.js                         # React Entry Point
│   ├── 📜 index.js                       # App Entry Point
│   ├── 📜 main.js                        # Electron Main Process
│   └── 📜 SystemListener.js              # System Event Handler
│
├── 📜 forge.config.js                    # Electron Forge Configuration
├── 📜 LICENSE                            # License File
├── 📜 package.json                       # Project Configuration
├── 📜 README.md                          # Project Documentation
└── 📜 README-EN.md                       # Project Documentation (English)
 ```

## Supported Platforms

- **Windows** (*x64*)
- **macOS** (*arm64*, M1 and above)

**Coming Soon**: macOS(x86) Linux

## Contribution

***Your contributions can enhance the quality of this program!***  

We deeply appreciate feedback and assistance from talented individuals.  
Feel free to suggest improvements or highlight areas that need refinement!

## Installation / Execution
Download the appropriate precompiled binary from the [Release Page](https://github.com/WareAoba/Paraglide/releases).

- **Windows**:
 - Install **Paraglide-win32-x64-setup.exe**.
 - Automatically registered in the program group.

- **macOS**:

 - Mount **Paraglide-darwin-arm64.dmg**.
 - Copy **Paraglide.app** to **~/Applications**.
 - Follow the instructions to enable **accessibility** and **input monitoring** permissions.

## Running in Dev Mode / Building

***(Prerequisites: Node.js)***

**Dev Mode**:

1. Clone the repository:

   ```bash
   git clone https://github.com/WareAoba/Paraglide
   ```

 2. Switch to the **development** branch:
  
   ```bash
   git checkout -b development
   ```

 3. Install NPM in root directory of the project:

   ```bash
   git clone https://github.com/WareAoba/Paraglide
   ```

 4. Run the program with the following command:
   
   ```bash
   npm run dev
   ```

 **Building and Compiling**:

 - Run the following command to create a build:(**may not have been tested** for compilation.)

  ```bash
  npm run make
  ```


## Recent Updates
 ### Latest Release: 0.2.0beta


 1. **Line Mode**: Added a mode to process text on a line-by-line basis instead of by paragraphs.
 2. **List View**: Added a mode that allows viewing all paragraphs by scrolling instead of showing previous/current/next paragraphs.
 3. **Page Number Logic** Improvements:
     - Extended regex for page number detection.
     - Detect page numbers attached to paragraphs.
     - Fixed bugs related to empty pages.
4. **Redux** introduced.
5. **Drag & Drop** added.

## Features in Development

 1. Search Function: Search text/paragraphs and jump to the desired paragraph.
 2. Photoshop Mode: Automatically input text layer creation using Photoshop API.
 3. Click-to-Jump in the overlay window.
 4. UI Icons: From pause/resume buttons to future buttons.
 5. User Guide: Plan to write a detailed manual for the program.
 6. File Editing: Simple modifications like renaming files or editing paragraph content.
 7. Multilingual Support: Planned to support English and Japanese first.

## Known Issues

 1. Overlay layout misalignment: All paragraphs should have equal spacing, but the gaps between previous/current and current/next are unusually wide. I'm currently unsure how to fix this.
 2. Unexpected bugs may have occurred during logic modification. Please report any issues!

## License

 The majority of the code for this program was generated using **GitHub Copilot Chat**.

 The program and its source code are distributed under the **MIT License**.
