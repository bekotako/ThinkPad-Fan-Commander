❄️ NoteFlow: The Ultimate Laptop Command Center
Transcend the limits of your BIOS. Control your hardware. Extend your lifespan.

NoteFlow is a next-generation, open-source system utility designed to bypass aggressive thermal throttling policies and locked battery configurations found in modern laptops (Lenovo, HP, Dell, Asus, and more).

Unlike standard fan control software, NoteFlow employs a Hybrid Intelligence Engine and an aggressive Persistence Loop to force hardware compliance, ensuring your settings stick even when the BIOS tries to override them.

⚡ Why NoteFlow? (Comparison)
Most fan control software fails because modern BIOS watchdogs are aggressive. NoteFlow is built differently.

<img width="867" height="462" alt="image" src="https://github.com/user-attachments/assets/5a3c9e64-1209-46a4-ad47-2da4bd7e6347" />

🧠 Under the Hood: The Hybrid Architecture
NoteFlow is not just a script; it is built upon a scalable, multi-layered architecture designed for universality.
graph TD;

    A[Launch NoteFlow] --> B{Local Config Exists?};
    B -- YES --> C[Load Precise JSON Profile];
    B -- NO --> D[Activate AI Detective];
    D --> E[Analyze System Vendor];
    E --> F[Apply Heuristic Heuristic Profile];
    C --> G[CORE ENGINE];
    F --> G;
    G --> H[Persistence Loop (Fan)];
    G --> I[WMI & PowerCfg (Battery)];
    
1. The Configuration Layer (Universal Support)
NoteFlow utilizes a robust JSON-based configuration system. It scans the Configs/ directory for a model-specific file (e.g., HP_OMEN_15.json).

Scalability: Supporting a new laptop is as simple as adding a single JSON file. No code changes required.

Current Library: Includes optimized support for 300+ Laptop Models converted from legacy databases.

2. The AI Detective (Heuristic Fallback)
If no configuration file is found, NoteFlow doesn't fail. It activates its internal heuristic engine:

It detects the manufacturer (Lenovo, Dell, Asus, etc.).

It applies the most statistically probable register addresses for that brand.

Result: It works "out of the box" on untasted hardware.

3. The "Nuclear" Battery Method
Standard Windows APIs often hide the Battery Cycle Count. NoteFlow spawns a background thread that interfaces directly with the Windows Power Configuration (PowerCfg) subsystem to parse raw XML reports, delivering 100% accurate Cycle Counts and Real-Time Health data that even OEM software often hides.

✨ Key Features
🌪️ Advanced Thermal Control
Pure Manual Mode: Direct access to EC registers. Set fans from Silent (0%) to TURBO JET (100% Disengaged).

Anti-Throttling: Prevents performance drops during gaming by forcing maximum cooling before the CPU hits thermal limits.

🔋 Battery Mastery
Charge Thresholds: Set a Start Limit (e.g., 40%) and Stop Limit (e.g., 80%). Keeping the battery away from 100% can double its lifespan.

Smart Presets: One-click toggles for Travel Mode (100%) and Desktop Mode (60%).

💻 System Dashboard & UX
Live Monitoring: Real-time visualization of CPU, RAM, and Disk loads.

Global Hotkeys: Control your fan speed while in-game using Ctrl + Alt + 1/2/3.

System Tray: Minimizes silently to the tray with status indication.

Dual Language: Native English and Turkish support.

📥 Installation
Go to the releases page.

Download the latest NoteFlow_vX.X_Release.zip.

Extract the folder to a safe location.

Run NoteFlow_vX.X.exe as Administrator.

Admin rights are mandatory for low-level hardware access (InpOut32).

🔮 Future Roadmap
The architecture of NoteFlow allows for massive expansion. Future goals include:

☁️ Cloud Auto-Sync: Automatically download missing config files from the GitHub repository upon launch.

📈 Custom Fan Curves: Graphical UI to draw temperature/speed curves (PID Controller).

🔌 Power Plan Sync: Automatically switch Windows Power Plans based on Fan Modes.

⚠️ Hardware Disclaimer
NoteFlow interacts directly with your laptop's Embedded Controller (EC) via port 0x62 and 0x66. While the application includes safety features (such as reverting to BIOS Auto-Mode upon exit), you use this software at your own risk. We are not responsible for hardware damage caused by disabling thermal protections or overriding fan speeds for extended periods without monitoring.

👨‍💻 Contributing
Got a new laptop model?

Find your register values.

Create a JSON file in the Configs folder.

Submit a Pull Request!

License: MIT License

VirusTotal Scan Result: https://www.virustotal.com/gui/file/b2bfabeaf524a8e42a84323ce1cd6abb74d5c3a3fc31ad595ace52b94ccfe539/detection
