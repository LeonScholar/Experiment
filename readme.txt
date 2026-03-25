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

🚀 How to Run the Experiment (Mandatory Steps)
🚀 实验运行指南（必读步骤）
Due to the large file size of experimental assets (145MB), the source code and the media assets are hosted separately in this repository. To run the experiment correctly, please follow these steps:
由于实验素材文件较大（145MB），源代码与媒体资源在本仓库中分开托管。为确保程序正常运行，请遵循以下步骤：

Step 1: Download the Source Code
步骤 1：下载源代码
Download the project files (including js/, readme.txt, and Experiment English Version.html) by clicking the green "Code" button and selecting "Download ZIP", or by cloning the repository.
点击绿色的 "Code" 按钮并选择 "Download ZIP"（或通过 Git 克隆仓库），下载项目基础文件（包括 js/ 文件夹、readme.txt 和 Experiment English Version.html）。

Step 2: Download the Assets from "Releases"
步骤 2：从 "Releases" 下载资源包
Locate the "Releases" section on the right side of this page. Download the assets.zip (or the file named under the DATA tag).
在页面右侧找到 "Releases" 区域。下载 assets.zip（或 DATA 标签下的资源包）。

Step 3: Organize Files
步骤 3：整理文件路径
Unzip the assets and move the DATA/ and lootbox/ folders into the root directory of the project. Your final directory structure should look like this:
解压资源包，并将 DATA/ 和 lootbox/ 文件夹移动到项目的根目录下。最终的目录结构应如下所示：

Plaintext

/Your-Project-Folder
  ├── js/
  ├── DATA/ (From Releases)
  ├── lootbox/ (From Releases)
  ├── Experiment English Version.html
  └── readme.txt
Step 4: Run the Task
步骤 4：运行实验任务
Open Experiment English Version.html in a modern web browser (Chrome or Edge recommended) to begin the task.
在现代浏览器（推荐 Chrome 或 Edge）中打开 Experiment English Version.html 即可开始实验任务。
