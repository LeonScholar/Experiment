Loot Box Behavioral Task
Overview
This repository contains the source code for a web-based behavioral experiment designed to investigate individual value assessment, curiosity, and decision-making (Willingness-to-Pay, WTP) in the context of virtual loot boxes.
The program is built using React and Tailwind CSS, offering high-precision timing and an immersive user interface suitable for both laboratory and online data collection.

Experimental Procedure
The experiment follows a structured cognitive paradigm:
Fixation: A central crosshair for visual orientation.
Induction (Stimuli Presentation): Display of a "Mystery Capsule" alongside rarity and winning probability cues (Silhouettes).
Confidence Assessment: Participants provide a Subjective Probability Judgment on their perceived chance of winning.
Decision Task (WTP): Participants indicate their Willingness-to-Pay by setting a maximum bid amount.
Outcome Anticipation: A standardized animation period to maintain engagement and measure anticipatory states.
Feedback: Presentation of the trial outcome (Win/Loss) and reward (Experimental Currency).

Key Features
High-Precision Timing: Utilizes performance.now() for millisecond-accurate Response Time (RT) and stimulus onset recording.
Random Incentive System: Implements a trial-randomization payout logic to ensure incentive compatibility and ecological validity.
Zero-Dependency Deployment: The entire experiment is contained within a single HTML file (utilizing CDN for libraries), making it easy to deploy and reproduce.

Data Structure
The program exports data in .csv format with the following primary variables:
Phone_Number: Unique participant identifier (anonymized in sample data).
Trial: Sequential trial index.
Confidence_Val: Subjective probability rating (0–100%).
Bid_Amount: Maximum willingness-to-pay (WTP).
Outcome_Win: Binary outcome of the trial (1 = Win, 0 = Loss).
RT Variables: Precise timestamps for every phase transition (Fixation to Result).

Intellectual Property & Disclaimer
This project is for academic and non-commercial research purposes only.
Original Assets: All creature silhouettes and monster designs used in this repository are original graphical assets created for this research.
Trademark Disclaimer: This program utilizes a "Pokémon-inspired" gamification theme to enhance participant engagement. However, it is NOT affiliated with, endorsed by, or associated with Nintendo, Creatures Inc., or GAME FREAK Inc. The terms "Pokémon" or "Poké Ball" (if referenced in documentation) are used descriptively for research context under fair use for academic study.
Copyright: The source code is provided under the MIT License.

Experimental Assets (Stimuli)
Due to file size constraints, the visual stimuli required for this experiment (the /Data folder) are not included in this GitHub repository.
For Reviewers: Please download the Data.zip archive provided in the Supplementary Materials (Appendix) of the manuscript. Extract the contents into a folder named Data in the project root directory.
For Other Researchers: To utilize this program, you must create a directory named Data and populate it with your own image assets (PNG format). The program expects:
chest.png: The icon for the loot box.
1.png through 50.png: The creature/item images corresponding to the card pool defined in the code.

How to Run (Offline Support)
This version of the experiment is designed to run in a fully offline environment once all necessary assets are downloaded. To ensure the program functions correctly, please maintain the following directory structure:

Required File Structure:
/LootBox_Experiment_Root
│
├── Experiment_English_Version.html  (Main entry file)
│
├── /js                              (Static Library Folder)
│   ├── tailwindcss.js
│   ├── react.production.min.js
│   ├── react-dom.production.min.js
│   └── babel.min.js
│
└── /Data                            (Experimental Stimuli Folder)
    ├── chest.png                    (The loot box icon)
    └── 1.png, 2.png, ... 50.png     (Creature images)

Instructions:
Download all files: Ensure the js folder (containing the 4 required JavaScript libraries) and the Data folder (containing images) are in the same directory as the HTML file.
No Internet Required: You do not need an active internet connection to run the experiment, as all dependencies are loaded locally.
Browser: Open Experiment_English_Version.html in a modern web browser (Chrome or Firefox recommended).
Full-Screen Mode: Click the "Full-screen & Preload" button to start. Adjust the browser zoom (Ctrl + Scroll Down) if the UI elements exceed your display area.