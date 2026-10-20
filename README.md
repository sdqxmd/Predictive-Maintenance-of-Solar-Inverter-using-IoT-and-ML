<!-- HEADER -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:0F766E,100:FACC15&height=120&section=header" alt="Solar yellow and teal wave header" />

<h1 align="center">☀️ Predictive Maintenance of Solar Inverter</h1>

<h3 align="center">Using IoT &amp; Machine Learning</h3>

<p align="center">
  <b>MATLAB/Simulink · Data Generation · ML Training · Hardware · IoT</b>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&duration=2800&pause=1200&color=14B8A6&center=true&vCenter=true&width=850&height=60&lines=Simulate+healthy+and+faulty+inverter+operation.;Generate+data.+Train+models.+Evaluate+predictions.;From+simulation+to+hardware+and+IoT+monitoring." alt="Animated introduction to simulation, data generation, machine learning, and hardware validation" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PROJECT-Final_Year-0891B2?style=for-the-badge&labelColor=161B22" alt="Final-year project" />
  <img src="https://img.shields.io/badge/STATUS-In_Progress-F59E0B?style=for-the-badge&labelColor=161B22" alt="Project in progress" />
  <img src="https://img.shields.io/badge/NEXT-Hardware_%26_IoT-14B8A6?style=for-the-badge&labelColor=161B22" alt="Hardware and IoT planned after simulation validation" />
</p>

<p align="center">
  <a href="https://github.com/sdqxmd/Predictive-Maintenance-of-Solar-Inverter-using-IoT-and-ML">
    <img src="https://img.shields.io/badge/Explore_Repository-161B22?style=for-the-badge&logo=github&logoColor=14B8A6" alt="Explore the project repository" />
  </a>
  <a href="https://github.com/sdqxmd/Predictive-Maintenance-of-Solar-Inverter-using-IoT-and-ML/issues">
    <img src="https://img.shields.io/badge/Ideas_%26_Discussion-0F766E?style=for-the-badge&logo=github&logoColor=white" alt="Share project ideas or open an issue" />
  </a>
</p>

<p align="center">
  <a href="#overview">Overview</a>
  &nbsp;•&nbsp;
  <a href="#simulation">Simulation</a>
  &nbsp;•&nbsp;
  <a href="#dataset">Dataset</a>
  &nbsp;•&nbsp;
  <a href="#machine-learning">Machine Learning</a>
  &nbsp;•&nbsp;
  <a href="#hardware-iot">Hardware &amp; IoT</a>
  &nbsp;•&nbsp;
  <a href="#roadmap">Roadmap</a>
</p>

---

<!-- OVERVIEW -->
<a name="overview"></a>
<h2 align="center">🔍 Understanding Inverter Health Through Data</h2>

<p align="center">
  This ongoing final-year project explores
  <b>predictive maintenance for a solar inverter</b>
  through MATLAB/Simulink modeling, simulation-generated datasets,
  machine learning, and a planned hardware implementation with IoT monitoring.
</p>

<p align="center">
  The current work focuses on generating data from
  <b>healthy and faulty inverter operation</b>
  and using an expanding dataset to train and evaluate machine-learning models.
</p>

<p align="center">
  Fault studies include <b>DC-link capacitor degradation</b>
  and <b>IGBT/MOSFET switching faults</b>.
  Random Forest and LSTM approaches are being explored for fault analysis,
  with remaining useful life estimation as a further research objective.
</p>

<p align="center">
  <b>
    First, develop and validate the simulation and ML workflow.
    Then, extend the approach to hardware measurements and IoT monitoring.
  </b>
</p>

---

<!-- PROJECT PHASES -->
<h2 align="center">🧭 Two Phases, One Connected Goal</h2>

<table align="center">
  <tr>
    <td width="50%" align="center" valign="top">
      <h3>🖥️ Phase 1 · Simulation &amp; ML</h3>
      <p>
        <img src="https://img.shields.io/badge/STATUS-ONGOING-F59E0B?style=flat-square&labelColor=161B22" alt="Simulation and machine learning are ongoing" />
      </p>
      <p>
        Develop the inverter model.<br />
        Generate healthy and faulty operating data.<br />
        Expand and prepare the training dataset.<br />
        Train models and evaluate fault analysis.
      </p>
      <p>
        <code>MATLAB</code>
        <code>Simulink</code>
        <code>Data Generation</code>
        <code>ML</code>
      </p>
    </td>
    <td width="50%" align="center" valign="top">
      <h3>🔌 Phase 2 · Hardware &amp; IoT</h3>
      <p>
        <img src="https://img.shields.io/badge/STATUS-PLANNED-0891B2?style=flat-square&labelColor=161B22" alt="Hardware and IoT are planned" />
      </p>
      <p>
        Develop the hardware prototype after simulation validation.<br />
        Acquire physical measurements.<br />
        Integrate networked monitoring and logging.<br />
        Evaluate models using hardware data.
      </p>
      <p>
        <code>Sensing</code>
        <code>Data Acquisition</code>
        <code>IoT</code>
        <code>Validation</code>
      </p>
    </td>
  </tr>
</table>

---

<!-- SIMULATION -->
<a name="simulation"></a>
<h2 align="center">⚡ Inside the MATLAB/Simulink Model</h2>

<p align="center">
  <a href="./images/predictivemaintenancesolarinvertermodel.jpg">
    <img
      src="./images/predictivemaintenancesolarinvertermodel.jpg"
      width="1100"
      alt="MATLAB Simulink solar inverter model showing a PV source, boost converter, DC link, PWM-controlled full bridge, output filter, load, and RMS and THD measurements"
    />
  </a>
</p>

<p align="center">
  <sub>
    Current simulation model · Click the image to inspect the full diagram.
  </sub>
</p>

<table align="center">
  <thead>
    <tr>
      <th align="center">Model Section</th>
      <th align="center">Role</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>☀️ PV Source</b></td>
      <td align="center">Represents the solar source with irradiance and temperature inputs.</td>
    </tr>
    <tr>
      <td align="center"><b>🔋 DC–DC Boost Stage</b></td>
      <td align="center">Conditions the PV-side DC voltage before the inverter stage.</td>
    </tr>
    <tr>
      <td align="center"><b>⚡ DC Link</b></td>
      <td align="center">Connects the converter and inverter stages through a DC energy buffer.</td>
    </tr>
    <tr>
      <td align="center"><b>🔄 Full-Bridge Inverter</b></td>
      <td align="center">Uses four controlled switches to produce an AC output from the DC supply.</td>
    </tr>
    <tr>
      <td align="center"><b>〰️ PWM Generation</b></td>
      <td align="center">Uses reference and carrier signals to generate inverter switching commands.</td>
    </tr>
    <tr>
      <td align="center"><b>🔌 Output Filter &amp; Load</b></td>
      <td align="center">Includes an LC output filter and a resistive load.</td>
    </tr>
    <tr>
      <td align="center"><b>📊 Measurements</b></td>
      <td align="center">Includes voltage observation, RMS measurement, and THD monitoring.</td>
    </tr>
  </tbody>
</table>

<p align="center">
  <b>The model is being developed as the foundation for data generation and fault studies.</b>
</p>

---

<!-- FAULT STUDIES -->
<h2 align="center">🩺 What Is Being Investigated?</h2>

<table align="center">
  <tr>
    <td width="33%" align="center" valign="top">
      <h3>🟢 Healthy Operation</h3>
      <p>
        Establish reference behavior for the inverter
        and characterize its signals under normal operating conditions.
      </p>
    </td>
    <td width="33%" align="center" valign="top">
      <h3>🟡 Capacitor Degradation</h3>
      <p>
        Study how DC-link capacitor degradation
        affects inverter signals and potential condition indicators.
      </p>
    </td>
    <td width="33%" align="center" valign="top">
      <h3>🔴 Switching Faults</h3>
      <p>
        Investigate IGBT/MOSFET switching faults
        and their effects on inverter operation and output waveforms.
      </p>
    </td>
  </tr>
</table>

<p align="center">
  <b>Research question:</b>
  Which measurable changes help distinguish normal operating variation
  from developing faults?
</p>

---

<!-- DATASET -->
<a name="dataset"></a>
<h2 align="center">🗂️ Building the Dataset in MATLAB</h2>

<p align="center">
  <b>Simulation is also the project's data source.</b>
</p>

<p align="center">
  Data is being generated through MATLAB/Simulink runs
  and used for machine-learning training.
  The dataset is being expanded to support analysis across
  multiple operating conditions and fault scenarios.
</p>

<h3 align="center">Dataset Coverage Being Developed</h3>

<table align="center">
  <thead>
    <tr>
      <th align="center">Category</th>
      <th align="center">Intended Coverage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>Operating Conditions</b></td>
      <td align="center">Variation in irradiance, temperature, and load conditions.</td>
    </tr>
    <tr>
      <td align="center"><b>System Condition</b></td>
      <td align="center">Healthy operation, capacitor degradation, and switching-fault scenarios.</td>
    </tr>
    <tr>
      <td align="center"><b>Time-Series Signals</b></td>
      <td align="center">Logged inverter signals for waveform and temporal analysis.</td>
    </tr>
    <tr>
      <td align="center"><b>Candidate Features</b></td>
      <td align="center">RMS values, THD, ripple measures, and other signal statistics.</td>
    </tr>
    <tr>
      <td align="center"><b>Labels &amp; Metadata</b></td>
      <td align="center">Simulation run identifiers, operating settings, fault type, and fault parameters.</td>
    </tr>
  </tbody>
</table>

<h3 align="center">Data Preparation Workflow</h3>

1. Define the operating conditions and fault scenario.
2. Run the MATLAB/Simulink model.
3. Log the selected signals and their timestamps.
4. Associate each run with its scenario labels and parameters.
5. Prepare signal features or time-series windows for model training.
6. Keep independent runs available for validation and testing.

<p align="center">
  <b>
    Dataset development focuses on varied operating scenarios,
    meaningful labels, and traceable simulation runs.
  </b>
</p>

---

<!-- MACHINE LEARNING -->
<a name="machine-learning"></a>
<h2 align="center">🧠 From Inverter Signals to Machine Learning</h2>

<p align="center">
  Model training is ongoing using the simulation-generated dataset.
  <b>Random Forest</b> and <b>LSTM</b> approaches are being explored
  for different ways of learning from inverter behavior.
</p>

<table align="center">
  <thead>
    <tr>
      <th align="center">Approach</th>
      <th align="center">Input Representation</th>
      <th align="center">Research Focus</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>🌳 Random Forest</b></td>
      <td align="center">Extracted signal features and operating-condition information.</td>
      <td align="center">Fault classification and investigation of useful condition indicators.</td>
    </tr>
    <tr>
      <td align="center"><b>🔁 LSTM</b></td>
      <td align="center">Ordered sequences of inverter measurements or condition indicators.</td>
      <td align="center">Temporal fault analysis and exploration of degradation trends.</td>
    </tr>
  </tbody>
</table>

<h3 align="center">📏 Evaluation Plan</h3>

- Split data by independent simulation runs before creating overlapping windows.
- Fit preprocessing steps using the training data.
- Evaluate fault classification with precision, recall, F1-score, and a confusion matrix.
- Test performance on operating conditions reserved for evaluation.
- Assess transfer to measured hardware data during the hardware phase.

<h3 align="center">⏳ Remaining Useful Life Exploration</h3>

<p align="center">
  <b>Remaining useful life (RUL) estimation is an exploratory objective.</b>
  It requires suitable degradation histories or lifetime data,
  together with an appropriate definition of failure.
  Healthy/faulty labels alone do not establish the time remaining before failure.
</p>

<p align="center">
  Dataset statistics, model configurations, and validated performance results
  will be documented as experiments are completed.
</p>

---

<!-- WORKFLOW -->
<h2 align="center">🔄 How the Project Develops</h2>

```mermaid
flowchart TD
    A["MATLAB / Simulink model"] --> B["Healthy operating runs"]
    A --> C["Fault scenarios"]

    B --> D["Labeled simulation dataset"]
    C --> D

    D --> E["ML training and evaluation"]
    E --> F{"Validation criteria met?"}

    F -->|Refine| A
    F -->|Yes| G["Hardware measurements — planned"]

    G --> H["IoT monitoring — planned"]
    G -.->|Compare and retrain| E
```

<p align="center">
  Simulation and ML validation guide the transition to hardware.
  Hardware measurements will then support further model evaluation and refinement.
</p>

---

<!-- HARDWARE AND IOT -->
<a name="hardware-iot"></a>
<h2 align="center">📡 Next Phase: Hardware &amp; IoT</h2>

<p align="center">
  Hardware implementation is planned after simulation validation.
  This phase will extend the study to physical measurements
  and investigate how the developed models perform on measured data.
</p>

<table align="center">
  <thead>
    <tr>
      <th align="center">Planned Area</th>
      <th align="center">Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>🔌 Inverter Prototype</b></td>
      <td align="center">Establish a physical platform for experimental validation.</td>
    </tr>
    <tr>
      <td align="center"><b>📏 Sensing &amp; Acquisition</b></td>
      <td align="center">Collect relevant electrical measurements and operating information.</td>
    </tr>
    <tr>
      <td align="center"><b>🗃️ Measurement Logging</b></td>
      <td align="center">Record timestamped data for analysis and comparison with simulation.</td>
    </tr>
    <tr>
      <td align="center"><b>🌐 IoT Connectivity</b></td>
      <td align="center">Transfer measurements and condition information for remote monitoring.</td>
    </tr>
    <tr>
      <td align="center"><b>📊 Monitoring Interface</b></td>
      <td align="center">Visualize measurements, trends, and model outputs.</td>
    </tr>
    <tr>
      <td align="center"><b>🧪 Model Validation</b></td>
      <td align="center">Compare predictions with experimental observations and refine models where required.</td>
    </tr>
  </tbody>
</table>

<p align="center">
  Hardware components, communication choices, and deployment details
  will be documented during this phase.
</p>

---

<!-- TOOLS -->
<h2 align="center">🛠️ Tools &amp; Methods</h2>

<table align="center">
  <thead>
    <tr>
      <th align="center">Tool / Method</th>
      <th align="center">Role in the Project</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>MATLAB</b></td>
      <td align="center">Data generation support, processing, analysis, and visualization.</td>
    </tr>
    <tr>
      <td align="center"><b>Simulink</b></td>
      <td align="center">Inverter modeling, simulation, and investigation of fault scenarios.</td>
    </tr>
    <tr>
      <td align="center"><b>Signal Analysis</b></td>
      <td align="center">Waveform inspection and development of condition indicators.</td>
    </tr>
    <tr>
      <td align="center"><b>Random Forest</b></td>
      <td align="center">Feature-based fault-analysis approach under exploration.</td>
    </tr>
    <tr>
      <td align="center"><b>LSTM</b></td>
      <td align="center">Sequence-based analysis approach under exploration.</td>
    </tr>
    <tr>
      <td align="center"><b>Hardware &amp; IoT</b></td>
      <td align="center">Planned physical validation, data acquisition, and remote monitoring.</td>
    </tr>
  </tbody>
</table>

---

<!-- ROADMAP -->
<a name="roadmap"></a>
<h2 align="center">🚧 Project Roadmap</h2>

- [x] Develop an initial MATLAB/Simulink solar inverter model.
- [ ] Complete validation of the simulation across selected operating conditions.
- [ ] Expand and document the healthy and faulty simulation dataset.
- [ ] Complete ML training experiments and model comparisons.
- [ ] Evaluate models using independent simulation runs.
- [ ] Investigate RUL estimation using suitable degradation or lifetime data.
- [ ] Develop the hardware prototype.
- [ ] Integrate IoT data logging and monitoring.
- [ ] Evaluate and refine models using hardware measurements.
- [ ] Publish results, reproducibility details, and project documentation.

<p align="center">
  <b>Current focus:</b>
  simulation development, MATLAB-generated data,
  dataset preparation, and machine-learning training.
</p>

---

<!-- REPOSITORY MATERIALS -->
<h2 align="center">📂 Planned Repository Additions</h2>

<p align="center">
  This repository documents an ongoing project.
  Supporting files will be added as they are prepared for sharing.
</p>

<table align="center">
  <thead>
    <tr>
      <th align="center">Material</th>
      <th align="center">Planned Contents</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center"><b>Simulation Models</b></td>
      <td align="center">Simulink models, configuration details, and model parameters.</td>
    </tr>
    <tr>
      <td align="center"><b>Data Generation</b></td>
      <td align="center">Scripts, scenario definitions, and signal-logging instructions.</td>
    </tr>
    <tr>
      <td align="center"><b>Datasets</b></td>
      <td align="center">Data samples, field descriptions, labels, and generation metadata.</td>
    </tr>
    <tr>
      <td align="center"><b>ML Experiments</b></td>
      <td align="center">Preprocessing, training workflows, model settings, and evaluation results.</td>
    </tr>
    <tr>
      <td align="center"><b>Hardware &amp; IoT</b></td>
      <td align="center">Component details, schematics, acquisition code, and monitoring documentation.</td>
    </tr>
  </tbody>
</table>

---

<!-- LEARNING OUTCOMES -->
<h2 align="center">📚 Learning Through the Project</h2>

<table align="center">
  <tr>
    <td width="50%" align="center" valign="top">
      <h3>⚡ Power Electronics &amp; Modeling</h3>
      <p>
        Solar inverter operation<br />
        DC–DC conversion and PWM<br />
        Simulation-based fault studies<br />
        RMS, THD, and waveform analysis
      </p>
    </td>
    <td width="50%" align="center" valign="top">
      <h3>🧠 Data &amp; Intelligent Monitoring</h3>
      <p>
        Simulation-generated datasets<br />
        Feature extraction and sequence modeling<br />
        ML training and evaluation<br />
        Hardware measurements and IoT integration
      </p>
    </td>
  </tr>
</table>

---

<!-- COLLABORATION -->
<h2 align="center">🤝 Ideas, Feedback &amp; Collaboration</h2>

<p align="center">
  Suggestions are welcome on inverter modeling, fault representation,
  dataset design, ML evaluation, and hardware validation.
</p>

<p align="center">
  When discussing an experiment, include the operating conditions,
  model settings, observed behavior, and relevant plots or data.
</p>

<p align="center">
  <a href="https://github.com/sdqxmd/Predictive-Maintenance-of-Solar-Inverter-using-IoT-and-ML/issues">
    <img src="https://img.shields.io/badge/Share_an_Idea-0F766E?style=for-the-badge&logo=github&logoColor=white" alt="Share an idea through GitHub issues" />
  </a>
</p>

---

<!-- AUTHOR -->
<h2 align="center">👨‍💻 Mohammad Sadique</h2>

<p align="center">
  Electrical Engineering · Jamia Millia Islamia, New Delhi
</p>

<p align="center">
  Exploring the connection between
  <b>power electronics, simulation, machine learning, and embedded systems</b>.
</p>

<p align="center">
  <a href="https://github.com/sdqxmd">
    <img src="https://img.shields.io/badge/GitHub-161B22?style=for-the-badge&logo=github&logoColor=14B8A6" alt="Mohammad Sadique on GitHub" />
  </a>
  <a href="https://www.linkedin.com/in/mdsdq/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge" alt="Mohammad Sadique on LinkedIn" />
  </a>
  <a href="mailto:mohdsadique6970942@gmail.com">
    <img src="https://img.shields.io/badge/Email-0F766E?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Mohammad Sadique" />
  </a>
</p>

<h3 align="center">⭐ Follow the Project as It Develops</h3>

<p align="center">
  Star the repository if you are interested in
  solar inverter monitoring and predictive-maintenance research.
</p>

<p align="center">
  <a href="https://github.com/sdqxmd/Predictive-Maintenance-of-Solar-Inverter-using-IoT-and-ML">
    <img src="https://img.shields.io/badge/Star_This_Project-FACC15?style=for-the-badge&logo=github&logoColor=161B22" alt="Star this project on GitHub" />
  </a>
</p>

<p align="center">
  <b>Simulate the system. Learn from the data. Validate with hardware.</b>
</p>

<!-- FOOTER -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:0F766E,100:FACC15&height=90&section=footer" alt="Solar yellow and teal wave footer" />
