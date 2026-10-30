<div align="center">

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/header.svg" alt="Muneer Ahmed Khokhar — Mechatronics, AI and Robotics" width="100%"/>

<a href="https://www.linkedin.com/in/muneer-ahmed-khokhar-b06368398"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=071A2B" alt="LinkedIn"/></a>
<a href="https://www.youtube.com/@ailearning-v4u"><img src="https://img.shields.io/badge/YouTube-Projects-FF0000?style=for-the-badge&logo=youtube&logoColor=white&labelColor=071A2B" alt="YouTube"/></a>
<a href="mailto:muneerahmedkhokhar53@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-FF7A3D?style=for-the-badge&logo=gmail&logoColor=white&labelColor=071A2B" alt="Email"/></a>
<img src="https://komarev.com/ghpvc/?username=muneerahmedkhokhar53-wq&label=Profile%20views&color=0A6B78&style=for-the-badge&labelColor=071A2B" alt="Profile views"/>

<br/><br/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/terminal.svg" alt="Terminal: who I am, what I focus on, and what I am looking for" width="100%"/>

<br/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/div-arch.svg" alt="System architecture" width="100%"/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/pipeline.svg" alt="Closed-loop pipeline: sense, perceive, decide, act, with feedback" width="100%"/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/div-projects.svg" alt="Project index" width="100%"/>

</div>

| ID | Project | What it does | Stack | Loop |
|:--:|---|---|---|:--:|
| `R-01` | [Hand Teleoperation: KUKA iiwa](https://github.com/muneerahmedkhokhar53-wq/hand-teleoperation-kuka-iiwa) | Webcam hand tracking drives a simulated robot arm and gripper for pick-and-place. | Python · MediaPipe · OpenCV · PyBullet | 1 → 4 |
| `R-02` | [Arm Kinematics: DH, FK & IK](https://github.com/muneerahmedkhokhar53-wq/Arm-Kinematics-DH-Forward-Inverse-) | Forward and inverse kinematics using Denavit–Hartenberg methods. | Python · Robotics | 4 |
| `V-01` | [Cybernetic AR HUD](https://github.com/muneerahmedkhokhar53-wq/Cybernetic_AR_Hud_Project) | Interactive vision HUD with hand gestures and optional perception modules. | Python · OpenCV · MediaPipe | 1 → 2 |
| `V-02` | [Face Recognition Attendance](https://github.com/muneerahmedkhokhar53-wq/face-recognition-attendance-System) | Computer-vision attendance prototype. | Python · OpenCV · YuNet · LBPH · MediaPipe | 1 → 3 |
| `A-01` | [RAG System + Evaluation Harness](https://github.com/muneerahmedkhokhar53-wq/RAG-system-with-an-evaluation-harness) | Document-grounded question answering with citations and a repeatable evaluation workflow. | Python · Retrieval · Evaluation | 3 |
| `A-02` | [Multi-Agent AI Research Assistant](https://github.com/muneerahmedkhokhar53-wq/Multi-Agent-AI-Research-Assistant) | Searches, reads, drafts, and critiques source-backed reports. | Python · LangChain · Streamlit | 3 |

> Loop = which stages of the pipeline above the project covers. Features and maturity vary; each repository documents its setup, limitations, and current status.

<details>
<summary><b>Kinematics core: how every arm project starts</b></summary>

<br/>

```python
import numpy as np

def dh(theta, d, a, alpha):
    """Standard Denavit–Hartenberg transform: Rz(θ)·Tz(d)·Tx(a)·Rx(α)."""
    ct, st, ca, sa = np.cos(theta), np.sin(theta), np.cos(alpha), np.sin(alpha)
    return np.array([[ct, -st*ca,  st*sa, a*ct],
                     [st,  ct*ca, -ct*sa, a*st],
                     [0,      sa,     ca,    d],
                     [0,       0,      0,    1]])

def forward(joints):            # joints = [(θ, d, a, α), ...]
    T = np.eye(4)
    for j in joints:
        T = T @ dh(*j)
    return T                    # base → end effector
```

</details>

<div align="center">

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/div-stack.svg" alt="Tech stack" width="100%"/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/stack.svg" alt="Technology stack grouped by capability" width="100%"/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/div-telemetry.svg" alt="Live telemetry" width="100%"/>

<a href="https://github.com/muneerahmedkhokhar53-wq"><img height="190" src="https://github-readme-stats.shion.dev/api?username=muneerahmedkhokhar53-wq&show_icons=true&rank_icon=github&bg_color=030D16&title_color=19E3D1&text_color=B8D4DB&icon_color=FF7A3D&border_color=14586B&hide_border=false" alt="GitHub stats"/></a>
<a href="https://github.com/muneerahmedkhokhar53-wq"><img height="190" src="https://github-readme-stats.shion.dev/api/top-langs/?username=muneerahmedkhokhar53-wq&layout=compact&bg_color=030D16&title_color=19E3D1&text_color=B8D4DB&icon_color=FF7A3D&border_color=14586B&hide_border=false" alt="Top languages"/></a>

<img src="https://streak-stats.demolab.com/?user=muneerahmedkhokhar53-wq&hide_border=false&background=030D16&border=14586B&stroke=14586B&ring=FF7A3D&fire=FF7A3D&currStreakNum=19E3D1&currStreakLabel=19E3D1&sideNums=B8D4DB&sideLabels=7FF5E8&dates=4F7F8C" alt="Contribution streak" width="100%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=muneerahmedkhokhar53-wq&bg_color=030D16&color=19E3D1&line=FF7A3D&point_color=FFFFFF&area=true&area_color=0A6B78&title_color=19E3D1&hide_border=true" alt="Contribution activity graph" width="100%"/>

<img src="https://github-profile-trophy.vercel.app/?username=muneerahmedkhokhar53-wq&theme=darkhub&no-frame=true&no-bg=true&margin-w=6&column=7" alt="GitHub trophies" width="100%"/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/div-contact.svg" alt="Open channel" width="100%"/>

</div>

```text
ENGINEERING PROTOCOL
1. build the smallest testable version first
2. document install, config, controls, and known limits
3. prefer measured results over unsupported performance claims
4. treat privacy and safe operation as design requirements,
   especially for camera-based systems
```

**Currently exploring:** robotics and AI integration · reliable computer-vision pipelines · robot kinematics and control · evaluation methods for AI applications

<div align="center">

<a href="https://www.linkedin.com/in/muneer-ahmed-khokhar-b06368398"><img src="https://img.shields.io/badge/LinkedIn-Muneer%20Ahmed%20Khokhar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=071A2B" alt="LinkedIn"/></a>
<a href="https://www.youtube.com/@ailearning-v4u"><img src="https://img.shields.io/badge/YouTube-AI%20Learning-FF0000?style=for-the-badge&logo=youtube&logoColor=white&labelColor=071A2B" alt="YouTube"/></a>
<a href="mailto:muneerahmedkhokhar53@gmail.com"><img src="https://img.shields.io/badge/Gmail-muneerahmedkhokhar53-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=071A2B" alt="Email"/></a>

<br/><br/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/footer.svg" alt="Engineering intelligent systems, one experiment at a time" width="100%"/>

</div>

<!-- Optional: Buy Me a Coffee. Replace YOUR_USERNAME (no spaces) and uncomment.
<a href="https://buymeacoffee.com/YOUR_USERNAME"><img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" alt="Buy Me a Coffee"/></a>
-->
