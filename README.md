# Central Vision Loss Reading Experiment – PsychoPy

## Overview

This repository contains the implementation of **Task 1 – Reading**, developed as part of my **MSc Thesis at Politecnico di Torino**, investigating the effects of simulated **Central Vision Loss (CVL)** on reading performance using **HoloLens 2 eye-tracking**.

The experiment compares two conditions:

- **Condition 1 – CVL**: Simulated central vision loss induced via **HoloLens 2**
- **Condition 2 – NV**: Normal vision without visual impairment simulation

Participants performed the reading task under both conditions while wearing **HoloLens 2** for continuous eye-tracking acquisition.

---

### Experimental Tasks

Each participant performed the reading task twice:

- Once under **CVL**
- Once under **NV**

To prevent memorization effects:

- Texts were **never repeated** between conditions  
- Stimulus sets were counterbalanced across participants  

---

## Task 1 – Reading

### Software Implementation

- **Python 3.8.10**
- **PsychoPy Toolbox**
- Developed using **Visual Studio Code**

The experimenter manually advanced stimuli using the **spacebar**, ensuring:

- Strict control of stimulus timing  
- Precise synchronization with eye-tracking data  

---

## Stimuli Structure

Two reading sub-tasks were implemented:

### Task 1a – Standard Texts

- 20 texts  
- 6 lines per text  
- 20–25 characters per line  
- Mixed semantic fields:
  - Science  
  - Daily life  
  - Horror  
  - Abstract thoughts  

Nonsensical phrases were intentionally included to prevent intuitive word completion under simulated scotoma.

### Task 1b – Numerical Texts

- 20 texts  
- 3 lines per text  
- Numbers embedded within sentences  
- Participants instructed to read **only the numbers** in the order they appeared  

---

## Text Organization and Counterbalancing

The repository contains two stimulus folders:

- `texts1/`
- `texts2/`

Each folder includes:

- **40 `.txt` files**
  - 20 standard texts
  - 20 numerical texts

To ensure proper randomization and counterbalancing:

- For **half of the participants**, `texts1` was used in the **CVL condition** and `texts2` in **NV**
- For the remaining half, the assignment was reversed

This design ensured that:

- No participant read the same text twice  
- Order effects were minimized  
- Learning and memorization biases were controlled  

---

## Trial Sequence

Each sub-task followed this sequence:

1. **START screen**
2. Text presentation
3. Pause screen with fixation dash (horizontal line aligned with the first word)
4. Next text

The fixation screen helped participants reorient attention between trials.

---

## Data Collection

For each text, the following variables were recorded:

- **Timestamp at text onset**
- **Timestamp at text offset**
- **Reading duration**
- Continuous **eye-tracking recording** via HoloLens 2

---

## Notes

- Raw experimental data are **not included** in this repository.
- This task is part of a broader multimodal AR-based experimental framework including:
  - Scotoma simulation in Unity  
  - Visual search task in Unity  
  - Eye-tracking data processing in Python  

---

## Author

**Robjona Toska**  
MSc Biomedical Engineering  
Politecnico di Torino
