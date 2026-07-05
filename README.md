# Shubhan Mital – Projects & Academic Portfolio

• Email: [shubhanmital@gmail.com](mailto:shubhanmital@gmail.com) 
• GitHub: [Shubhanflash22](https://github.com/Shubhanflash22) 
• LinkedIn: [linkedin.com/in/shubhan-mital](https://www.linkedin.com/in/shubhan-mital/) 
• Portfolio: [shubhanflash22.github.io](https://shubhanflash22.github.io/)

---

My passion sits at the intersection of **mathematics, machine learning, and optimization** — I'm drawn less to using models off the shelf and more to understanding the principles that make them work, especially when that understanding can be applied to real-world constraints like energy, cost, and time.

I'm currently pursuing my **MS in Machine Learning and Data Science (ECE) at UC San Diego**, where I work with the **Yuanyuan Lab** on energy-aware scheduling for electric construction equipment. I've built a multi-stage computer vision pipeline (**YOLOv8, DeepSORT, 3D ResNet-18**) to convert 34+ hours of construction site footage into per-activity energy profiles, hitting **88.81% recognition accuracy** across activity classes. I'm now benchmarking deterministic vs. stochastic MPC formulations to schedule mobile EV charging in real time — work that's been featured by UC San Diego. Math has always been core to how I approach this: I hold an **M.Sc. in Mathematics** alongside my **B.E. in Electrical and Electronics Engineering from BITS Pilani**.

Before UCSD, I spent just over a year as a **Data Scientist at Piramal Pharma**, where I owned the end-to-end lifecycle of ML forecasting models (predicting inventory stock-out/expiry risk 24 months out), built scalable data pipelines on Azure Databricks and Snowflake that cut processing time by 60%, and automated pricing workflows that reduced turnaround time by 70%. Earlier, as a **Software Development Engineer Intern at Amazon**, I built data validation and pipeline auditing tools that caught discrepancies across 5+ downstream pipelines, helping prevent losses of up to $5 million.

Outside of work, I like building end-to-end systems that combine optimization with modern ML: an agentic AI tool (**LangGraph + MILP**) for residential solar and battery sizing, a multimodal attention-detection system fusing facial and audio signals for classroom engagement, and research into noise-conditioned controllability in text-to-image diffusion models.

I'm always happy to talk optimization, applied ML, or anything at the intersection of the two — feel free to reach out.

---

## 🛠 Skills Matrix

<details>
<summary>Click to expand</summary>

| Category                        | Skills / Tools                                                                   |
| ------------------------------- | -------------------------------------------------------------------------------- |
| **Programming Languages**       | Python, Java, C, C++, Scala, R, MATLAB, SQL, ROS/ROS2, Linux                     |
| **Frameworks & Libraries**      | Pandas, NumPy, SciPy, Scikit-learn, TensorFlow, Keras, PyTorch, Hugging Face, OpenCV, MediaPipe, Librosa |
| **AI/ML Techniques**            | Computer Vision, NLP, Deep Learning, Generative & Diffusion Models, Sequence Modeling (LSTM/BiLSTM), Reinforcement Learning, Predictive Modeling |
| **Robotics & Control**          | SLAM (VI-SLAM, ICP, Occupancy Grid Mapping), Kalman/Extended Kalman Filtering, Motion Planning (Weighted A*), Dynamic Programming, Model Predictive Control, Optimal Control (CEC/GPI), Sensor Fusion, Embedded C |
| **Optimization & Solvers**      | Convex/Nonlinear Optimization, MILP, CasADi, IPOPT, Game Theory                  |
| **LLMs & Agents**               | LangGraph, RAG, Ollama, vLLM, LLaMA, Whisper, Stable Diffusion (Diffusers)       |
| **Cloud & Tools**               | AWS (Lambda, S3, CloudFormation), Azure (Databricks, ADF, Functions), Snowflake, Docker, Kubernetes, GTSAM |
| **Software Engineering**        | Full-stack development, CI/CD pipelines, ETL, Automation                         |

</details>

---

## 📂 Projects Portfolio
_Focus Areas: Machine Learning, Statistical Learning, Autonomous Systems, Energy Systems Optimization, Data-Driven Modeling_

<details>
<summary>Click to expand for all projects</summary>

---
### 🚜 Excavator Activity Recognition & Energy-Aware Charging — Research at Yuanyuan Lab, UC San Diego
**Oct 2025 – Ongoing**
* Built a multi-stage computer-vision pipeline chaining YOLOv8 detection, DeepSORT multi-object tracking, a physics-constrained finite state machine, and transfer-learned 3D ResNet-18 spatiotemporal classification with automated CVAT annotation, converting **34+ hours** of raw construction-site footage into per-subactivity energy profiles for mobile electric excavator charging dispatch.
* Achieved **88.81%** recognition accuracy across 5 activity classes, surpassing a prior 3-class benchmark of 86.7%; applied Bayesian regression for hidden-state power estimation and built automated tooling for class-balanced clip extraction.
* Benchmarking deterministic certainty-equivalent MPC against scenario-based stochastic MPC over a 24-hour dispatch window to produce real-time mobile charging schedules that curb on-site battery depletion, demand charges, and grid carbon impact.

**Tools:** Python, PyTorch, YOLOv8, 3D ResNet, DeepSORT, OpenCV, CVAT, MPC, Bayesian Regression, Pandas, SciPy

---
### 🤖 Projects of ECE 276B - Planning & Learning in Robotics
**Apr 2026 – Jun 2026**
* Implemented dynamic programming for the Door-Key grid problems, computing optimal action sequences across 7 known and randomized MiniGrid environments.
* Built a 3D motion planner using weighted A* on a 26-connected grid with a parametric slab segment–AABB collision engine and forward-greedy path smoothing, clearing 7 environments (including dynamic multi-goal scenes) within strict per-goal timing budgets.
* Solved infinite-horizon stochastic optimal control for a differential-drive robot tracking a lemniscate trajectory via Receding-Horizon Certainty Equivalent Control (CasADi/IPOPT) with slack-variable obstacle avoidance and Generalised Policy Iteration on a discretised error-state MDP.
* **Homework:** worked through the planning & control foundations — deterministic shortest-path and label-correcting search, Markov Decision Processes with value and policy iteration, LQR, and reinforcement learning.

**Tools:** Python, NumPy, CasADi, IPOPT, Matplotlib, Gym-MiniGrid

---
### 👀 Project of ECE 228 - Machine Learning for Physical Applications
**Apr 2026 – Jun 2026**
* Built **StayTuned**, a multimodal attention-detection system fusing a visual pipeline (MediaPipe landmarks → EAR/MAR/gaze/head-pose features → Bidirectional LSTM on DAiSEE) with an audio pipeline (Whisper transcription → ~75 acoustic features → LR/RF with speaker-aware GroupKFold) to classify students/drivers as attentive vs. distracted in real time.
* Fused per-interval scores via grid-searched weighting (0.85 video / 0.15 audio), supporting offline batch and live webcam + microphone inference, validated against ground-truth spreadsheets.
* Deployed a companion ESP32 + SSD1306 OLED and piezo-buzzer hardware alert for real-time attention warnings.
* **Homework:** implemented sparse linear regression (ISTA/LASSO regularization paths, GWAS marker selection) and Poisson GLMs via maximum likelihood; compared MLP vs. Transformer models for multivariate time-series forecasting; and built Neural ODEs and Fourier Neural Operators for the 1D wave equation with super-resolution analysis.

**Tools:** Python, TensorFlow, Keras, PyTorch, MediaPipe, OpenCV, Whisper, Scikit-learn, Librosa, ESP32/Arduino

---
### 🎨 Project of ECE 271B - Statistical Learning II
**Jan 2026 – Mar 2026**
* Researched noise-conditioned controllability and reliable random seeds in text-to-image diffusion models, building on the *All Seeds Are Not Equal* (ICLR 2025) NPNet framework.
* Built a modular, resume-safe seed-mining pipeline generating 62k+ images with Stable Diffusion across numeracy and spatial prompt grids, with multi-GPU seed sharding, atomic writes, and OOM-fallback batching.
* Containerized the workload with Docker (CUDA) and deployed single- and multi-GPU Kubernetes jobs with persistent storage for large-scale generation.
* **Homework:** implemented eigenface PCA, Regularized Discriminant Analysis, and Gaussian classifiers for face recognition, and trained MLPs with backpropagation on MNIST (ReLU vs. sigmoid, SGD, learning-rate studies).
* **Homework:** built AdaBoost with decision stumps (one-vs-all ensembles with margin analysis) and kernel SVMs (LibSVM) on MNIST.

**Tools:** Python, PyTorch, Hugging Face Diffusers, Stable Diffusion, Accelerate, Docker, Kubernetes, MATLAB, LibSVM

---
### 🛰️ Projects of ECE 276A - Sensing & Estimation in Robotics
**Jan 2026 – Mar 2026**
* Implemented quaternion-based 3D orientation tracking from IMU data using Projected Gradient Descent on the SO(3) manifold with gyroscope-bias learning, then stitched calibrated camera frames into equirectangular panoramas.
* Built a full 2D SLAM pipeline: differential-drive odometry, SVD-based ICP scan matching, log-odds occupancy grid mapping with Bresenham raycasting, RGB-D texture mapping, and GTSAM factor-graph optimization with loop-closure detection.
* Developed a Visual-Inertial SLAM EKF on SE(3) fusing IMU prediction with stereo landmark updates — Shi-Tomasi + Lucas-Kanade feature tracking, stereo triangulation, a Mahalanobis innovation gate, and a numerically-verified left-perturbation SE(3) pose Jacobian with sparse joint pose-landmark covariance.
* **Homework:** derived the core estimation theory — Bayesian and Gaussian filtering, rigid-body motion and rotations on SO(3)/SE(3) with quaternions, and the Kalman, Extended Kalman, and particle filters.

**Tools:** Python, PyTorch, NumPy, SciPy, OpenCV, GTSAM

---
### ⚡ Project of ECE 285 - Data Science & AI for Smart Grids (LLMs & Agents)
**Jan 2026 – Mar 2026**
* Built **SolarAgent**, an agentic LLM tool (LangGraph) pairing a natural-language front-end with a MILP optimization backend to recommend residential solar PV **and battery** sizing for real San Diego households.
* Formulated and solved a mixed-integer linear program (HiGHS) over an 8760-hour annual dispatch, jointly sizing panels and batteries from real hardware catalogs (Tesla Powerwall, Enphase, SolarEdge) under TOU/demand tariffs, roof-area limits, budgets, federal ITC, and EV charging.
* Also built a zero-cloud LLM + TF-IDF RAG advisor (Track A) for PV sizing, batch-analyzing 30 San Diego neighbourhoods with configurable local backends (Ollama/vLLM), and evaluated the agent against fixed baselines on Kubernetes.
* Presented a paper on RLHF / InstructGPT (*Training Language Models to Follow Instructions with Human Feedback*).

**Tools:** Python, LangGraph, HiGHS (MILP), Ollama, vLLM, LLaMA, RAG (TF-IDF), NumPy, Pandas, Kubernetes

---
### 🎲 Project of ECE 225A - Prob Stats for Data Science
**Sept 2025 – Dec 2025**
* Built an end-to-end statistical learning pipeline to predict national happiness scores by integrating multi-source global datasets (World Happiness Report, World Bank, CO₂ emissions, population data).
* Applied feature engineering and statistical validation, including factor analysis for maternal health indicators, VIF-based multicollinearity control, and Bonferroni correction for multiple hypothesis testing.
* Trained and evaluated regression models (Ridge, Random Forest, Gradient Boosting), achieving R² = 0.88 and identifying key predictors such as social support, GDP per capita, and life expectancy.
* Conducted rigorous exploratory data analysis and scaling comparisons (Standard, Robust, MinMax), extracting interpretable insights on economic, social, and environmental drivers of well-being.

**Tools:** Python, Overleaf(Latex)

---
### 📉 Projects of ECE 271A - Statistical Learning 1
**Sept 2025 – Dec 2025**
* Implemented Bayesian classifiers for cheetah vs. grass image segmentation using DCT features, achieving minimum probability-of-error decisions via histogram-based and Gaussian models.
* Modeled high-dimensional data with multivariate Gaussians (ML & MAP) and demonstrated the curse of dimensionality, reducing error from 5.52% (64D) to 3.11% (selected 8D features).
* Developed fully Bayesian predictive classifiers with informative and neutral priors, showing improved robustness on small datasets and convergence behavior as sample size increased.
* Trained Gaussian Mixture Models using Expectation-Maximization, analyzing initialization sensitivity and model complexity to identify an optimal bias–variance tradeoff (C = 8 components, ~4% error).

**Tools:** Matlab, Overleaf(Latex)

---
### 🚗 Project of ECE 148 - Introduction to Autonomous Vehicles
**Sept 2025 – Dec 2025**
* Designed an autonomous roadside mechanic that detects broken-down vehicles via blinking hazard lights and navigates to park safely behind them using multi-sensor fusion.
* Implemented a ROS2-based distributed system with a Jetson Nano (bird’s-eye vision) and Raspberry Pi (on-vehicle perception & control) communicating through custom publish-subscribe nodes.
* Trained and deployed a Roboflow/YOLO deep learning model (~90% accuracy) on an OAK-D camera to detect the rear of vehicles and compute angular offsets for PD-based navigation.
* Integrated LiDAR-based distance estimation and vision-based control to enable precise stopping behavior behind the disabled vehicle while reducing false positives using HSV filtering, temporal analysis, and FFT-based blink detection.

**Tools:** Python, Linux, ROS2, OpenCV, Path Planning, Sensor Integration, Embedded C, Computer Vision, Deep Learning, Roboflow, YOLO, Jetson Nano, Raspberry Pi, LIDAR, GPS, VESC, DC-DC converter

---
### ⚡ Optimization of Renewable Energy Storage (ML & DL)
**Jan 2023 – May 2023**
* Modeled **ANN, LSTM, and RNN** to predict power loss at different states of charge and electrolyte flow rates.
* Improved accuracy of existing models by **40–70%**.
* Optimized energy storage systems for cost and efficiency.

**Tools:** Python, TensorFlow, PyTorch

---
### 🖥️ Client-Server System (Operating Systems)
**Mar 2023 – May 2023**
* POSIX-compliant multithreaded server with shared memory IPC.
* Stateless client-server communication: register, request, response, unregister.
* Logging of all intermediate states and request counts.

**Tools:** C, POSIX threads, Shared Memory

---
### 🔢 Matrix Calculations (Operating Systems)
**Jan 2023 – Mar 2023**
* POSIX program for 2D matrix operations using 1-to-1 pipe between controller & workers.
* Fork + multithreading for efficient row-wise calculation.
* Handled errors and signals robustly.

**Tools:** C, POSIX, Multithreading

---
### 📅 Time Table Scheduler
**Jan 2023 – May 2023**
* Scheduler for BITS community to manage availability and meetings.
* Members register as staff/students using BITS email.
* Set personal availability and view availability of others.

**Tools:** Java, Intellij, MySQL

---
### 📊 Implicit Finite Difference Scheme
**Jan 2023 – May 2023**
* Plotted central and implicit finite difference scheme results for 4 wave propagation speeds using **Richter wavelet**.

**Tools:** Python, MATLAB

---
### 🌬️ Power Electronic Converters in Wind Generators
**Jan 2023 – May 2023**
* Implemented **NPC converter** to increase output voltage vs. boost converter.
* Implemented **MMC converter** to improve efficiency of wind generation.

**Tools:** MATLAB Simulink, Power Electronics Toolbox

---
### 🧬 Predict Cancer (ML)
**Nov 2022 – Dec 2022**
* Aggregated 30+ feature variables, preprocessed, and analyzed patient data.
* Baseline logistic regression improved with Decision Trees, Naïve Bayes, and **SVM**.
* Achieved **>99% accuracy** after hyperparameter tuning.

**Tools:** Python, Scikit-learn, Pandas, NumPy

---
### ⌚ Human Activity Sensor for Smartwatches (ML)
**Oct 2022 – Nov 2022**
* Collected data from 30 smartwatch users.
* Preprocessed and trained model to predict wearer activity with high accuracy.
* Tested in real-world scenarios.

**Tools:** Python, Scikit-learn, Pandas

---
### 📖 Spell Checker & Dictionary Implementation 
**Nov 2022 – Dec 2022**
* Implemented **hash table-based spell checker**.
* Corrects common errors: swap, insert, delete, replace characters.

**Tools:** C++

---
### 💨 Wind Generation Forecasting
**Oct 2022 – Dec 2022**
* Developed ML model for wind power projections with superior accuracy vs. basic time series models.
* Used **BCD classifier + SVR** for non-stationarity and adaptability.
* 48-hour predictions outperform persistence model.
  
**Tools:** R

---

### 🟢 1-Bit Full Adder (Analog & VLSI Design)
**Nov 2022 – Dec 2022**
* Designed half-adder using **NAND, NOR, Inverter** gates at transistor-level CMOS.
* Combined two half-adders into 1-bit full adder.
* Optimized propagation delay and power efficiency.

**Tools:** LTSpice

---
### 🔢 Mathematical Models
**Aug 2022 – Dec 2022**
* Implemented **Piecewise Lagrange Linear and Quadratic approximations and interpolations**.

**Tools:** MATLAB

---
### 🏎️ Pit Stop Strategy in Motorsports(Game Theory)
**Mar 2022 – Apr 2022**
* Used game theory to predict optimal pit stops under dry, wet, and safety car conditions.
* Calculated **Nash equilibria** and payoffs for different tyre strategies.
* Applied model to real-life race scenarios.

**Tools:** Python, MATLAB

---
### ⏱️ Predict Waiting Time in Queuing Systems (ML & DL)
**Jan 2021 – May 2021**
* Neural network trained on bank queue data to predict waiting times (MAE: 2.68 minutes).
* Verified queue-specific networks using web app simulator.
* Generalizable to other industries.

**Tools:** Python, Keras, TensorFlow

---
## 🎓 Courses & Grades

<details>
<summary>Click to expand BITS Courses (GPA - <b>8.48 out of 10.00</b>)</summary>
  
| Code      | Course                             | Grade |
| --------- | ---------------------------------- | ----- |
| CS F111   | COMPUTER PROGRAMMING               | B     |
| CS F213   | OBJECT ORIENTED PROGRAMMING               | B     |
| CS F372   | OPERATING SYSTEMS                  | A-    |
| EEE F111  | ELECTRICAL SCIENCES                | B-    |
| EEE F211  | ELECTRICAL MACHINES                | B     |
| EEE F212  | ELECTROMAGNETIC THEORY               | A-    |
| EEE F214  | ELECTRONIC DEVICES                 | B-    |
| EEE F215  | DIGITAL DESIGN                     | A-    |
| EEE F241  | MICROPROCESSORS & INTERFACING            | B-    |
| EEE F242  | CONTROL SYSTEMS                    | B     |
| EEE F243  | SIGNALS & SYSTEMS                  | A-    |
| EEE F244  | MICROELECTRONIC CIRCUITS           | B     |
| EEE F311  | COMMUNICATION SYSTEMS              | A-    |
| EEE F312  | POWER SYSTEMS                      | B     |
| EEE F313  | ANALOG & DIGIT VLSI DESIGN            | A-    |
| EEE F341  | ANALOG ELECTRONICS                 | A-    |
| EEE F342  | POWER ELECTRONICS                  | B     |
| EEE F376  | DESIGN PROJECT                     | A     |
| EEE F424  | SMART GRID FOR SUSTAINABLE ENERGY      | A     |
| MATH F111 | MATHEMATICS I                      | B-    |
| MATH F112 | MATHEMATICS II                     | B     |
| MATH F113 | PROBABILITY & STATISTICS           | B     |
| MATH F211 | MATHEMATICS III                    | B     |
| MATH F212 | OPTIMIZATION                       | A-    |
| MATH F213 | DISCRETE MATHEMATICS               | B-    |
| MATH F214 | ELEMENTARY REAL ANALYSIS           | B-    |
| MATH F215 | ALGEBRA I                          | A-    |
| MATH F241 | MATHEMATICAL METHODS               | A     |
| MATH F242 | OPERATIONS RESEARCH                | B     |
| MATH F243 | GRAPHS AND NETWORKS                | B     |
| MATH F244 | MEASURE AND INTEGRATION              | CLR   |
| MATH F311 | INTRODUCTION TO TOPOLOGY           | C     |
| MATH F312 | ORDINARY DIFFERENTIAL EQUATIONS            | A-    |
| MATH F313 | NUMERICAL ANALYSIS                 | C     |
| MATH F341 | INTRODUCTION TO FUNCTIONAL ANALYSIS           | C     |
| MATH F342 | DIFFERENTIAL GEOMETRY              | A-    |
| MATH F343 | PARTIAL DIFFERENTIAL EQUATIONS             | B     |
| MATH F353 | STATISTICAL INFERENCING & APPLICATIONS            | A-    |
| MATH F366 | LABORATORY PROJECT                 | A     |
| MATH F432 | APPLIED STATISTICAL METHODS        | B     |
| BITS F110 | ENGINEERING GRAPHICS               | B     |
| BITS F111 | THERMODYNAMICS                     | B     |
| BITS F112 | TECHNICAL REPORT WRITING           | A-    |
| BITS F221 | PRACTICE SCHOOL I                  | A     |
| BITS F225 | ENVIRONMENTAL STUDIES              | GD    |
| BITS F232 | FOUNDATIONS OF DSA      | B     |
| BITS F314 | GAME THEORY AND ITS APPLICATIONS   | A     |
| BITS F385 | INTRODUCTION TO GENDER STUDIES            | A-    |
| BITS F412 | PRACTICE SCHOOL II                 | A     |
| BITS F413 | PRACTICE SCHOOL II                 | A     |
| BITS F464 | MACHINE LEARNING                   | B-    |
| CHEM F110 | CHEMISTRY LABORATORY               | A     |
| CHEM F111 | GENERAL CHEMISTRY                  | B-    |
| ME F110   | WORKSHOP PRACTICE                  | B     |
| PHY F110  | PHYSICS LABORATORY                 | A     |
| PHY F111  | MECHANICAL OSCILLATIONS & WAVES           | C     |
| BIO F110  | BIOLOGY LABORATORY                 | A     |
| BIO F111  | GENERAL BIOLOGY                    | C-    |
| GS F234   | DEVELOPMENT ECONOMICS              | B-    |
| HSS F248  | INTRODUCTION TO DISABILITY STUDIES | B-    |

</details>

<details>
<summary>Click to expand UCSD Courses (GPA - <b>3.83 out of 4.00</b>)</summary>
  
| Code      | Course                             | Grade |
| --------- | ---------------------------------- | ----- |
| CSE 252A  | COMPUTER VISION I                          | TBD    |
| ECE 143   | PROGRAMMING FOR DATA ANALYSIS              | TBD    |
| ECE 148   | INTRODUCTION TO AUTONOMOUS VEHICLES        | A      |
| ECE 225A  | PROBABILITY AND STATISTICS FOR DATA SCIENCE | B+    |
| ECE 228   | ML FOR PHYSICAL APPLICATIONS               | A      |
| ECE 269   | LINEAR ALGEBRA AND APPLICATIONS            | TBD    |
| ECE 271A  | STATISTICAL LEARNING 1                     | B+     |
| ECE 271B  | STATISTICAL LEARNING 2                     | A      |
| ECE 276A  | SENSING AND ESTIMATION IN ROBOTICS         | A      |
| ECE 276B  | PLANNING AND LEARNING IN ROBOTICS          | A      |
| ECE 285   | DATA SCIENCE AND AI FOR SMART GRIDS        | A      |
| ECE 285   | DEEP GENERATIVE MODELS                     | TBD    |

</details>

---
