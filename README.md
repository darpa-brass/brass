# Building Resource Adaptive Software Systems (BRASS) 

Modern-day software operates within a complex ecosystem of libraries, models, protocols and devices. Ecosystems change over time in response to new technologies or paradigms, as a consequence of repairing discovered vulnerabilities (security, logical, or performance-related), or because of varying resource availability and reconfiguration of the underlying execution platform. When these changes occur, applications may no longer work as expected because their assumptions on how the ecosystem should behave may have been inadvertently violated.

Ensuring applications can seamlessly continue to operate correctly and usefully in the face of such changes is a formidable challenge. Failure to effectively and timely adapt to ecosystem evolution can result in technically inferior and potentially vulnerable systems, but the lack of automated mechanisms to restructure and transform applications when changes do occur leads to high software maintenance costs and premature obsolescence of otherwise functionally sound systems. Neither of these outcomes is desirable and poses significant risk to economic productivity and cyber resilience.

Successfully adapting applications to an evolving ecosystem requires mechanisms to infer the impact of such evolution on application behavior and performance, automatically trigger transformations that beneficially exploit these changes and provide validation that these transformations are correct. To do so requires the ability to: (a) extract whole-system specifications over the entire software stack that can be used to define application-centric descriptions of the resources provided by the ecosystem; (b) leverage new programming abstractions, program analyses, and compilation methodologies to correlate application behavior with salient ecosystem changes; (c) develop semantics-preserving program transformations designed with adaptation in mind; and (d) exploit new runtime systems and virtual machine implementations structured to facilitate the efficient integration of these transformations.

The goal of the Building Resource Adaptive Software Systems program (BRASS) is to realize foundational advances in the design and implementation of long-lived, survivable and complex software systems that are robust to changes in the physical and logical resources provided by their ecosystem. These advances will necessitate integration of new resource-aware program abstractions and analyses, in addition to novel compiler and systems designs to trigger adaptive transformations and validate their effectiveness. 

# Teams

## Southwest Research Institute
### Adaptive Constraints Satisfaction in Flight Test Configuration and Vehicle Situational Awareness

### Project Overview
The Adaptive Constraints Satisfaction in Flight Test Configuration and Vehicle Situational Awareness (SIFT) team used their subject matter expertise in both flight test (based on the Integrated Network-Enhanced Telemetry (iNET) program) and ground vehicle instrumentation and network (based on the Vehicular Integration for C4ISR/EW Interoperability (VICTORY) program) to frame a series of military-relevant challenge problems for BRASS performers. THese challenge problems covered a number of scenarios, including static and dynamic scheduling of flight test transmissions, instrumentation configuration, and measurement processing. Over the course of the program, the SIFT team worked directly with performers to integrate and evaluate their technologies applied to these areas in flight test, and pursued solutions to VICTORY challenge problems directly. Additionally, the SIFT team was responsible for program evaluation of all team-specific challenge problems, which was done using a distributed cloud architecture.

### Major Accomplishments
The SIFT team worked together with five different BRASS performers to implement a total of eight different flight test scenarios. In total, BRASS technologies were successfully applied to TDMA transmission scheduling, dynamic spectrum sharing, flight test plan adaptation, bytecode repair in response to schema evolution, measurement fault detection and recovery, and program generation for measurement processing. The SIFT team successfully utilized natural language processing (NLP) to identify differences between to version sof the VICTORY specification and correlated the changes to the lines of VICTORY XML that need to, likewise, be changed. Additionally, the SIFT team successfully utilized latent direchlet allocation (LDA) to identify anomalies between the expected model of a VICTORY network and the live capture of a VICTORY network.

#### Repositories
[Challenge Problems](https://github.com/darpa-brass/challenge-problems)  
[Database Framework](https://github.com/darpa-brass/adaptive-constraint-satisfaction)  

## University of Washington
### Sandcat: Adaptive Visualization of Big Data

### Project Overview
The UW Sandcat project responded to (1) the rapid change in hardware, systems software, and application workloads; and (2) the trend towards increased complexity of computer systems, especially at the interfaces which were intended to hide the complexity. The rapid change requies adapting existing applications and infrastructure but the complexity makes the adaptation more difficult. The Sandcat project developed methods that analyze existing component and synthesize new ones. The Sandcat adaptations were semantic and mostly performerd offline. The goal was to aid programmers and system designers who currently adapt code by manually rewriting the code. The project selected problems from across the entire systems stack, from the CPU to compute kernels and data structures, and from disk devices to file systems and databases.

### Major Accomplishments
The synthesis technology developed by Sandcat reached parity with human programmers on about a dozen different programming tasks, which is a major milestone in this research area. Some problems solved by Sandcat have been automated for the first time. The human-parity results from the project enabled new adaptation of software to harware, including synthesis of (!) ultra-low-precision ML kernels (TVM), (2) surprising rewrites to floating-point expressions (Herbie), and (3) new mappins of computations onto GPUs not achievable by existing compuilers (Swizzle Inventor). The technology also synthesized artifacts that semantically summarize existing implementations, enabling (4) performance portability to new platforms and hardware (verified lifting), and (5) automatic authoring of memory models and file system crash consistency models (memSynth and Ferrite). These advances were enabled by new infrastructure, including (6) the Cozy synthesizer of data structures, (7) the Rosette generator of synthesizers, and (8) the Stacatto automatic checker of adaptation mechanisms. The results of verified lifting ship in a commercial photo editing product; the Rosette architecture is being used in the Synthetic Minds startup; and the ML kernels are being commercialized by OctoML.

## SRI International
### DyAdEm: Dynamic Adaptive Embeded Software

### Project Overview
The DyAdEm project is a collaboration between SRI International, Honeywell Research, the University of California Berkeley, and Boston University, directed at the compositional design of high-assurance adaptive cyber-physical systems. These systems consist of multiple physical and computational nodes, including sensors, actuators, and physical plant components. The focus of the project is on Dynamic Adaptive Embedded (DyAdEm) software that can adapt to vehicle specifics, terrain variations, changing operational constraints, wear and tear, sensor degradation and failure, new requirements, new components, and changes to the platform and environment. The adaptations include the use of learning-enabled components, virtual sensors, adaptive system identification, adaptive planning and control, and adaptive perception. Offline adaptations include those that allow sensors to be reconfigured through virtual sensors, the use of monitors to restrict behavior, inverse reinforcement learning to acquire new skills through training, retargeting high-level architectures to alternative platforms, and adapting from simulation to reality. Online adaptations allow state estimation and system identification to cope with error and uncertainty, and enable systems to replan based on local conditions, improve tracking by adjusting to lighting and weather conditions, and to switch between controllers based on perceived error. We have conducted adaptation experiments with robot vehicles such as the Segway RMP440LE and the F1tenth car. 

### Major Accomplishments
The achievements of the DyAdEm project include: Radler architecture definition language for adaptive cyber-physical systems; SOTER framework for runtime assurance; the Breach tool for runtime monitoring and diagnosis of STL properties; the SCENIC probabilistic language for scenario generation; virtual sensors that continuously correct for bias and variance; expectation maximization scheme for adaptive system identification and fault detection/correction; nested controller synthesis for multiple objective; efficient monitoring for Signal Temporal Logic properties; context-aware falsification of learning-enabled components; the SOLCAM adaptive sensor fusion method for combining primary and secondary sensors; resilient feature tracking through adaptive local luminosity; adaptive global+local planning/replanning; hybrid controller for Reach-Avoid specification combining pure pursuit with deep reinforcement learning; safety-aware apprenticeship learning; resilient LIDAR-based mapping and localization; and SPEC simulation metric for synthesizing safe (specification-aware) controllers under modeling and sensor uncertainty. 

## BAE Systems
### Regenerative, INtent-Guided Systems (RINGS)

### Project overview
Regenerative INtent Guided Systems (RINGS) is an application-neutral software adaptation environment that restores intent when behavior deviates due to changes in the computing or operational environment. Genetic algorithms, the core repair technology that allows RINGS to handle the "unknown-unknowns" of maintaining long-lived software, adapts the code to the new conditions restoring intent. The RINGS API migration tool, Software Search and Replace (SSR), enables automated changes to large code bases, freeing library maintainers from API backward compatability requirements. SSR edit rules, packaged with the new library, migrate client code to the new API. SSR rules use data types while matching and updating, reducing the false positives of text based updates. The AST-diff tool supports identification and creation of edit rules through examination of differences in abstract syntax trees of original and manually ported code. 

### Major Accomplishments
RINGS adaptation has repaired programs from the ManyBugs benchmark problems, including scaling to localize and repair a defect in PHP among 1M source lines of code. For a DoD fielded tracking application, RINGS automatically upgraded the messaging protocol from STANAG version 2 to version 3; and RINGS tunes the tracking parameters to automatically focus the track picture. RINGS reduced tracker memory usage by removing fields from data structures that do not affect intent. Beyond C/C++ applications, RINGS has also repaired a tracker algorithm implemented in the Coq functional language and adapted non-functional requirements of a formal specification by selecting alternate implementations while preserving correctness. The RINGS SSR API migration tool has migrated client application code from ROS1 to ROS2 for a subset of the API, and automatically secured the communication channels using ROS2 encryption capabilities. 

## Rice University
### Proteus: Cotrolling Resource-Adaptive Embedded Software

### Project Summary:
The Proteus project has developed a platform for constructing self-adaptive applications that uses  declarative specifications of the application developer's intent, expressed as constrained optimization problems, and meets these intents using feedback control that leverages machine-learning of the the application's behavior. This approach can exploit relationships between different aspects of the application's behavior to seamlessly enact trade0offs between measures such as quality, performance, and energy. This allows the system to be resilient to real0time changes in environmental conditions or goals. The intent specification language, library and runtime support dynamic, programmatic changes to the intent, as well as to the space of configurations considered by the controller. The platform has been evaluated by instru,enting several software applications that are relevant to the military, including video compression, radar signal processing, image matching, and radio bandwidth scheduling. The platform's viability has further been proved through porting to multiple embedded systems. In addition to the real-time resilience of our platform, we have also studied using new (weaker) memory models to improve the long-term resilience of platforms to changes in processor hardware.
 
 ### Major Accomplishments
Among the major accomplishments of the project is the creation of a programming language, based on the open-source and cross-platform version of Swift, which implements a novel programming model that permits fine-grained manual control over application configuration where necessary, and provides autonomous optimal control of the rest of the configuration. The project led to numerous advances in energy and performance-aware control for embedded and cloud computing applications, including an approach to online reconfiguration that combines feedback control with self-monitoring and machine-learned performance models. The project's inquiry into machine-learned surrogates for dynamic assurance led to novel results in prediction for complex dynamical systems. The project has also designed and formally characterized the Weak Memory Model (WMM) and contributed to the formalization of the open-source RISC-V memory model.


## Carnegie Mellon University
### Generating Hyper-Portable Future-Proof Computational Kernels with SPIRAL
http://www.spiral.net/software/brass.html

### Project Summary
Software implementations and algorithms that solve a particular problem are inherently not *future-proof* as an algorithm appropriate for the problem *and* execution environment has to be instantiated into software that locks in many choices. However, the actual *operation* - the answer for a given input - remains invariant through execution environment changes and changes in required fidelity. SPIRAL's layered approach to application specification leverages this insight: we capture the systematic process by which the specification of a desired operation is turned into an algorithm, and subsequently instantiated into an actual implementation. SPIRAL becomes akin to an installation/reconfiguration-time JIT that regenerates a tunable implementation for a given specification and execution target. To provide an even easier on-ramp for legacy code, a subset of the functionality is accessible through a delayed-evaluation interface using BLAS, LAPACK, FFTW and a subset of C as domain-specific specification language. The SPIRAL system is available under BSD open source license at www.spiral.net. 

### Major accomplishments
In the course of DARPA BRASS we demonstrated a true write-once-run-everywhere-(fast) capability for mission-critical code. Polar formatting synthetic aperture radar imaging running continuously at high performance and efficiency was moved across target hardware including CPUs with advanced instruction sets and field-programmable gate arrays (FPGAs) without interruption. New hardware was installed post deployment and the running software was adapted to the new execution environment dynamically without change in the source code. This demonstrated true forward compatibility to yet-unknown platforms. As final demonstration this technology was applied to the SwRI Flight Test setup, where the capabilities of legacy military hardware were enhanced by communication intercepting modules that partially computed and filtered the data as it was transmitted down from the flight platforom to the base station. The intercept/compute capability was parameterized and deployment-time reconfigurable to allow adaptation to missions as needed, and to provide capabilities beyond what the original hardware is capable of.

#### Repositories
[SPIRAL](https://github.com/spiral-software/spiral-software)  
[SPIRAL Hybrid Control Operator Language](https://github.com/spiral-software/spiral-package-hcol)  

## Raytheon BBN
### Interfaces, Models, and Monitoring for Resource-aware Transformations that Augment the Lifecycle of Systems (IMMoRTALS)

### Project Summary 
The Raytheon BBN Technologies-led IMMoRTALS project has adopted a broad approach to the software longevity goals set by BRASS, analyzing and addressing software adaptation through multiple categories of change drivers, including ongoing evolution of an application's external data formats, third-party libraries, hardware and infrastructure resource dependencies and extra-functional requirements. IMMoRTALS augments the software development and maintenance process by systematically collecting metadata through program analysis; augmenting that metadata with developer-provided information to identify what needs to be changed in the software and where; and finally effecting these changes, rebuilding and testing the rebuilt application. Together with a diverse array of both learning-based and analytic techniques integrated into the application's build system, this approach can detect and respond to a wide range of adaptive pressures efficiently. The IMMoRTALS team included Securboration, Oregon State University, University of California Riverside, and Vanderbilt University. 

### Major Accomplishments
The IMMoRTALS team developed and demonstrated a novel ontology-enabled automated software adaptation capability, including substitution and composition of annotated software components, to address changing requirements and resource provisions. Combined with variational analysis to select and validate software components, this framework has addressed non-trivial adaptive pressures common to many applications. We have successfully integrated learning-based techniques such as relational learning and deep learning using neural networks to adapt software to changing schema and APls. We have also demonstrated an innovative use of test-based program minimization in software adaptation by trading off application's requirements with changes in the software ecosystem. Last but not the least, we demonstrated automated source code transformation to adapt to changing API/usage protocols based on a pattern-based DSL specification of the changes. 

## Carnegie Mellon University
### Intelligent Model-Based Adaptation for Mobile Robotics

### Project Summary
The BRASS Model-based Adaptation for Robotic Systems (MARS) project explored a set of techniques that fundamentally raise the level of abstraction at which we build and evolve mobile robotics systems. Our approach builds mathematical models of the robot's components and the software that runs them, as well as the environment with which the robot interacts. The design intent captured by these models enables us to explore the space of adaptation at a much higher level than was previously possible, allowing the robot to adapt more autonomously to greater changes in its environment than was previously possible. 

### Major Accomplishments
The BRASS MARS project demonstrated multiple novel forms of adaptation. Our robots can automatically calibrate their sensors and can automatically learn to fix problems in the state machine transitions that drive their behavior. Models of the environment in which the robot operates, as well as models of the robot's power consumption, sensor accuracy, and more are used not just for autonomous navigation, but for reacting to changes in the robot's environment. These models are not fixed, however - our techniques including online learning of new models that capture the effect of changes to the robot and its environment on concerns such as power consumption. We have developed techniques that discover the architecture of running BRASS systems; these architectures can be incorporated as first-class models within the system, enabling software adaptations that change the connectivity of components or even support major platform changes without requiring corresponding major edits to the code. New components may be installed that have semantic mismatches with old components; our approach can automatically discover code updates that fix those semantic problems. Together, these advances enable robotics software to adapt, with minimal human effort, to a wide range of environmental and software changes that would require extensive engineering time in the previous state of the art.

## Charles River Analytics
### Probabilistic Representation of Intent Commitments to Ensure Software Survival (PRINCESS)

### Project Summary
Under Probabilistic Representation of Intent Commitments to Ensure Software Survival (PRINCESS), we have developed techniques to extend the lifespan of software using both offline processes that modify the software and online adaptation that changes the behavior of the software. Our offline processes begin with operating system (OS) adaptation where we synthesize an operating system for a new computer architecture, ensuring survival of the software through hardware changes. Offline processes also include adapting to replacement of a sensor with a new sensor, integrating information coming from the new sensor into the existing software. Finally, the offline process includes a program transformation that turns a legacy, non-adaptive software system into an adaptive system by increasing its range of behavior. Our online processes enable the software to adapt to perturbations in the syStern or the environment, such as degraded sensors, changing physical forces, or reduced power. 

### Major Accomplishments
We have demonstrated all our adaptations on UUV software. For our OS adaptation, we identified machine-dependent and machine-independent parts of an OS and developed formal languages to describe the machine-dependent parts, as well as the target hardware architecture. We developed a system that uses these formal languages to synthesize the machine-dependent parts for the target architecture. For sensor adaptation, we have developed methods that reconstruct the original sensor data when the sensor has degraded or been replaced with a new sensor. In collaboration with Southwest Research Institute, these methods have been applied to reconstruct flight test sensors when a sensor fails. Our sensor adaptation method have also been demonstrated on an unmanned undersea vehicle's velocity sensors in a realistic simulation. Meanwhile, the software transformations we have developed provide a powerful and general approach that can be applied to make a legacy software system adaptive. By combining program transformations to synthesize controls for the software with machine learning to learn how to optimize these controls in different situations, we are able to make the software flexible and resilient to perturbations. This software transformation and machine learning has been demonstrated on UUV software. Finally, working with SwRI, we have developed methods to transform and optimize flight test plans to maximize communication resource usage, enabling more test flights to be scheduled. 

#### Repositories
[PRINCESS CP1](https://github.com/darpa-brass/cra-princess-cp1)  
[PRINCESS CP2](https://github.com/darpa-brass/cra-princess-cp2)  
[PRINCESS CP3](https://github.com/darpa-brass/cra-princess-cp3)  
