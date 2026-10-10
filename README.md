### Hi, I'm Kuncheng (Quin) Wu 👋

**Embodied AI @ UC Berkeley · VLM post-training (SFT + RL) · embodied agents** · M.S. Civil & Environmental Engineering (Transportation Systems), 2026
Research with **Prof. Xuan Wang's group (Virginia Tech CS)** and the **Systems Cognition Engineering Lab (SCEL)**

I post-train VLM agents with **SFT and reinforcement learning (GRPO)** to look, call tools and answer on long video. Separately, I run prompted VLMs as **closed-loop policies** for drones and quadrupeds, and build the **synthetic-data and evaluation infrastructure** behind both.

🌐 **Portfolio:** [kunchengwu.github.io](https://kunchengwu.github.io)

---

#### 🔭 What I'm working on

- **Post-training a 9B VLM agent: SFT, then RL.** LoRA SFT on 2,955 tool-use trajectories: 69.7 / 64.9 / 55.1% accuracy on surgical video QA (CholecT50 / HeiChole / MultiBypass), +4.5 / +10.6 / +7.4 pts over matched answer-only SFT. Then GRPO with dynamic sampling on up to 12 A100s across preemptible Slurm jobs: 69.7 → 71.1% in-domain (McNemar p = .011); 74.4% with added evidence tools, on par with DeepSeek-V4.1-Flash using the same tools (73.3%).
- **VLMs as closed-loop robot policies.** Each step the model sees the robot's camera frame and returns a JSON action. Isaac Sim and SimWorld (Unreal Engine) tasks for Unitree Go2 navigation, drone inspection, and aerial-to-ground search-and-verify handoffs. Qwen, InternVL and DeepSeek policies compared on success, collisions, stopping, localization error and latency. On the public ESARBench UAV search-and-rescue benchmark (120 tasks), a claim → verify → commit agent reaches 18.5% success vs 10.4% for APEX with the same VLM, at 93% report precision.
- **Robot memory: answer, look again, or abstain?** A 760-query benchmark over a replayable dynamic household (RGB / depth / segmentation, visibility-derived memory), across 4 evidence states and 3 observation budgets.
- **Neural scene representations.** NeRF and 3D Gaussian Splatting from video, for persistent 3D world models.

#### 📄 Publications

- **VICO: Visual Environments Co-Evolving for Vision-Language Model Reasoning** — NeurIPS 2026 (Main Track, Poster)
  M. Lu, L. Zhu, O. Xiao, Y. Zhuang, Z. Wang, **K. Wu**, B. Liu, Y. Wang, C. Fleming, W. Shi, X. Wang · [arXiv](https://arxiv.org/abs/2610.10782)
- **Dynamic Estimation of Airport Taxiway Hotspots Using Spatio-Temporal Traffic and Kinematic Risk Modeling** — Accident Analysis & Prevention, 2026
  Q. Lyu\*, J. Zeng\*, **K. Wu**\*, J. Rakas† · \*co-first authors, †corresponding · [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7102038)

#### 🛠️ Toolkit

**VLMs & learning:** PyTorch · LoRA / SFT · GRPO · multi-node training (Slurm) · tool-use trajectories · VLM policy evaluation · vLLM · GNNs
**Simulation:** Isaac Sim · SimWorld · Unreal Engine / UnrealCV · multi-robot (drone + Unitree Go2)
**3D & world models:** NeRF · 3D Gaussian Splatting · scene graphs · Open3D
**Robot systems:** ROS 2 / ROS 1 · NVIDIA Orin NX · LiDAR–inertial SLAM · GIS
**Languages:** Python · C++ · R · MATLAB

#### 🛤️ Background

From transportation engineering (B.Eng. Tongji University; airport-siting GNNs, shared-micromobility optimization at Berkeley) to embodied AI, bridging physical infrastructure with embodied intelligence.

#### 📫 Contact

Open to full-time roles in robot learning, VLA and embodied foundation models.
forwu_clrs@berkeley.edu · [kunchengwu.github.io](https://kunchengwu.github.io)
<!-- Add when ready: LinkedIn, Google Scholar -->
