Cognitively-Adaptive Transparent VR System (CAT-VR)

A groundbreaking neuroadaptive VR system that integrates real-time EEG monitoring, LLM-based cognitive interpretation, and generative AI to create personalized mixed-reality environments.

Research Extension: This project extends the original fractal neurofeedback work by Salimi & Khosrowabadi with modern AI capabilities.

🌟 Features
🧠 Real-time EEG Integration: EMOTIV EPOC X support with cognitive state monitoring

🤖 LLM Cognitive Interpretation: Semantic understanding of brain states using large language models

🎮 Hierarchical Agentic Control: Multi-timescale adaptation (reflex, strategy, meta-learning)

🎨 Generative Content: AI-driven fractal and semantic visual generation

👓 Transparent VR: Mixed reality with adaptive environment blending

📊 Comprehensive Analytics: Real-time data logging and visualization

🎯 Research Applications
Cognitive Enhancement: Optimize focus, relaxation, and engagement

Mental Health: Anxiety reduction and stress management

Education: Adaptive learning environments

Professional Training: Cognitive load-optimized simulations

Neurorehabilitation: Personalized therapeutic interventions

🚀 Quick Start
Prerequisites
Python 3.9+

Unity 2022.3+

EMOTIV EEG Headset (optional - simulator included)

NVIDIA GPU (recommended for AI components)

Installation
Clone the repository

bash
git clone https://github.com/your-username/CAT-VR-System.git
cd CAT-VR-System
Install Python dependencies

bash
pip install -r requirements.txt
Setup Unity Environment

Open Unity Hub

Add the unity/ folder as a project

Install required packages: XR Interaction Toolkit, XR Plugin Management

Basic Usage
Start the Python backend

bash
python main.py --mode vr --config config/system_config.yaml
Launch Unity VR application

Open Assets/Scenes/MainScene.unity in Unity

Press Play or build for your VR platform

Begin cognitive adaptation

Put on your VR headset

The system will automatically detect and adapt to your cognitive state

📁 Project Structure
text
CAT-VR-System/
├── 📚 Documentation/
│   ├── RESEARCH_PROPOSAL.md
│   ├── API_REFERENCE.md
│   └── EXPERIMENTAL_PROTOCOLS.md
├── 🔧 Source Code/
│   ├── src/
│   │   ├── eeg_processing/      # EEG data acquisition and analysis
│   │   ├── cognitive_interpreter/ # LLM-based state interpretation
│   │   ├── agentic_controller/   # Hierarchical adaptation system
│   │   ├── generative_content/   # AI content generation
│   │   ├── vr_integration/       # Unity communication bridge
│   │   └── utils/               # Data logging and visualization
│   └── unity/                   # VR application source
├── ⚙️ Configuration/
│   └── config/                  # System configuration files
├── 🧪 Testing/
│   ├── tests/                  # Unit and integration tests
│   └── validation/             # Experimental validation scripts
├── 📊 Data/
│   ├── logs/                   # Session data and analytics
│   └── models/                 # Trained AI models
└── 📋 Examples/
    ├── demo_scripts/           # Demonstration scripts
    └── use_cases/              # Specific application examples
🔧 Core Components
1. EEG Processing Module
python
from src.eeg_processing.emotiv_reader import EmotivEEGReader

eeg_reader = EmotivEEGReader()
real_time_data = eeg_reader.get_multi_modal_data()
2. LLM Cognitive Interpreter
python
from src.cognitive_interpreter.llm_interpreter import CognitiveStateInterpreter

interpreter = CognitiveStateInterpreter()
cognitive_state = interpreter.analyze_state(eeg_data, eye_tracking, hrv_data)
3. Hierarchical Agentic Controller
python
from src.agentic_controller.hierarchical_controller import HierarchicalController

controller = HierarchicalController()
adaptation_decision = controller.process_cognitive_state(cognitive_state)
4. Generative Content System
python
from src.generative_content.content_manager import ContentManager

content_manager = ContentManager()
adaptive_content = content_manager.generate_content(adaptation_decision)
🎮 Unity VR Integration
The Unity project provides the VR interface with the following key components:

TransparentVROverlay.cs: Manages mixed reality blending

CognitiveLayer.cs: Base class for cognitive adaptations

FractalCognitiveLayer.cs: Adaptive fractal visualization

VRManager.cs: Main system controller

Building for Different Platforms
bash
# Oculus Quest
Unity -buildTarget android -exportPath ./Builds/Quest/

# Windows Mixed Reality  
Unity -buildTarget win64 -exportPath ./Builds/WMR/

# SteamVR
Unity -buildTarget win64 -exportPath ./Builds/SteamVR/
🔬 Research Validation
Experimental Protocols
The system includes predefined experimental protocols:

Focus Enhancement Protocol

Stress Reduction Protocol

Learning Optimization Protocol

Clinical Rehabilitation Protocol

Data Collection
All sessions automatically log:

Raw EEG data and derived metrics

Cognitive state interpretations

Adaptation decisions and parameters

User interaction data

System performance metrics

📈 Results Visualization
Built-in visualization tools for analyzing cognitive adaptation:

python
from utils.visualization import SessionAnalyzer

analyzer = SessionAnalyzer("session_data.h5")
analyzer.plot_cognitive_trajectory()
analyzer.generate_session_report()
🛠️ Development
Adding New Cognitive Strategies
Extend StrategyAgent:

python
class CustomStrategy(CognitiveStrategy):
    def __init__(self):
        super().__init__(
            name="custom_strategy",
            target_state={"focus": 0.8, "relaxation": 0.6},
            stimulus_parameters={"fractal_dim": 1.5, "color_scheme": "custom"},
            priority=7
        )
Register in configuration:

yaml
strategies:
  custom_strategy:
    target_state: {focus: 0.8, relaxation: 0.6}
    stimulus: {fractal_dim: 1.5, color_scheme: "custom"}
    priority: 7
Custom Content Generators
python
class CustomContentGenerator(ContentGenerator):
    def generate_adaptive_content(self, adaptation: Dict) -> Dict:
        # Implement custom content generation logic
        return custom_content
🧪 Testing
Run the comprehensive test suite:

bash
# Run all tests
pytest tests/ -v

# Test specific components
pytest tests/test_agentic_controller.py -v
pytest tests/test_cognitive_interpreter.py -v
pytest tests/integration/ -v
📊 Performance Metrics
The system tracks multiple performance indicators:

Cognitive State Accuracy: Comparison with ground truth measures

Adaptation Latency: Time from EEG input to VR adaptation

User Experience Metrics: SUS scores and subjective feedback

System Reliability: Uptime and error rates

🔗 Related Repositories
Core Dependencies
EMOTIV LSL Integration: Real-time EEG data streaming

Unity XR Toolkit: VR interaction framework

Stable Diffusion Unity: AI content generation

Complementary Projects
NeuroFeedback-BCI: Traditional neurofeedback implementation

EEG-ML-Pipeline: Machine learning for EEG analysis

VR-Cognitive-Assessment: VR cognitive testing protocols

📚 Publications & Citations
Original Research
bibtex
@article{salimi2023fractal,
  title={A Customized Closed-loop EEG-based Interface System to Adjust Focus, 
         Relaxation, and Engagement by Alteration of Visual Stimuli Complexity},
  author={Salimi, Mohammed Ali and Khosrowabadi, Reza},
  journal={Institute for Cognitive and Brain Sciences},
  year={2023}
}
CAT-VR Extension
bibtex
@software{catvr2024,
  title={Cognitively-Adaptive Transparent VR System (CAT-VR)},
  author={CAT-VR Research Team},
  url={https://github.com/your-username/CAT-VR-System},
  year={2024}
}
👥 Contributing
We welcome contributions from researchers and developers:

Fork the repository

Create a feature branch: git checkout -b feature/new-strategy

Commit changes: git commit -am 'Add new cognitive strategy'

Push to branch: git push origin feature/new-strategy

Submit Pull Request

Contribution Areas
New cognitive adaptation algorithms

Additional VR platform support

Enhanced AI models for state interpretation

Clinical validation studies

Performance optimization

📄 License


🤝 Research Collaboration
We actively collaborate with research institutions on:

Clinical Trials: Anxiety, ADHD, PTSD interventions

Educational Studies: Adaptive learning environments

Industrial Applications: Workforce training and safety

Technology Development: Next-generation BCI interfaces

Contact: salimiali74@gmail.com



🌟 Acknowledgments
This research extends the foundational work of:

Mohammed Ali Salimi - Original fractal neurofeedback research

