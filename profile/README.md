<div align="center">

<a href="https://github.com/muneerahmedkhokhar53-wq?tab=repositories"><img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/dashboard.svg" alt="Muneer Ahmed Khokhar: engineering profile dashboard with projects, pipeline coverage, stack and contact channels" width="100%"/></a>

<a href="https://www.linkedin.com/in/muneer-ahmed-khokhar-b06368398"><img src="https://img.shields.io/badge/LinkedIn-Connect-1E7BFF?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A0E1A" alt="LinkedIn"/></a>
<a href="https://www.youtube.com/@ailearning-v4u"><img src="https://img.shields.io/badge/YouTube-AI%20Learning-FF7A00?style=for-the-badge&logo=youtube&logoColor=white&labelColor=0A0E1A" alt="YouTube"/></a>
<a href="mailto:muneerahmedkhokhar53@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-00D4FF?style=for-the-badge&logo=gmail&logoColor=white&labelColor=0A0E1A" alt="Email"/></a>
<img src="https://komarev.com/ghpvc/?username=muneerahmedkhokhar53-wq&label=Profile%20views&color=1E7BFF&style=for-the-badge&labelColor=0A0E1A" alt="Profile views"/>

<br/><br/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/terminal.svg" alt="Terminal: who I am, what I focus on, and what I am looking for" width="100%"/>

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

> Loop = which pipeline stages the project covers (1 sense, 2 perceive, 3 decide, 4 act). Features and maturity vary; each repository documents its setup, limitations, and current status.

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

<a href="https://github.com/muneerahmedkhokhar53-wq"><img height="190" src="https://github-readme-stats.shion.dev/api?username=muneerahmedkhokhar53-wq&show_icons=true&rank_icon=github&bg_color=0A0E1A&title_color=FF7A00&text_color=C9D4E6&icon_color=00D4FF&border_color=1E2A3F&hide_border=false" alt="GitHub stats"/></a>
<a href="https://github.com/muneerahmedkhokhar53-wq"><img height="190" src="https://github-readme-stats.shion.dev/api/top-langs/?username=muneerahmedkhokhar53-wq&layout=compact&bg_color=0A0E1A&title_color=FF7A00&text_color=C9D4E6&icon_color=00D4FF&border_color=1E2A3F&hide_border=false" alt="Top languages"/></a>

<img src="https://streak-stats.demolab.com/?user=muneerahmedkhokhar53-wq&hide_border=false&background=0A0E1A&border=1E2A3F&stroke=1E2A3F&ring=FF7A00&fire=FF7A00&currStreakNum=00D4FF&currStreakLabel=00D4FF&sideNums=C9D4E6&sideLabels=8A97AD&dates=5B6A85" alt="Contribution streak" width="100%"/>

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

<br/>

<img src="https://raw.githubusercontent.com/muneerahmedkhokhar53-wq/muneerahmedkhokhar53-wq/main/assets/footer.svg" alt="Engineering intelligent systems, one experiment at a time" width="100%"/>

</div>
