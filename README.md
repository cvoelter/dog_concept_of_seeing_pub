# dog_concept_of_seeing

Data analysis of "Canine perspective-taking: The concept of seeing in dogs"

## Table of Contents

- [File Descriptions](#file-descriptions)
- [Data Variables](#data-variables)


## File Descriptions

- **`data/concept_of_seeing_test_phase.csv`**: This file contains behavioral data collected during the "Concept of Seeing" study.
- **`workspace/concept_of_seeing.RData`**: This file stores pre-processed data and the fitted models.
- **`functions/diagnostic_fcns.r`**: A script containing custom functions for diagnostics and assumption checks (function kindly provided by Roger Mundry).
- **`saves`** folder: Saved model results.
- **`graphics`** folder: Saved plots.  
-- **`choice_plot.png`**: Barplot showing the number of dogs by condition that approached the seen and unseen bowl first in the test phase (N per condition: control condition: 37 dogs; cue condition: 36 dogs).   
-- **`approach_plot.png`**: Barplot showing the number of dogs by condition that approached at least one of the bowls.  

---

## Data Variables

Descriptions of the variables included in the **`concept_of_seeing_test_phase.csv`** file:

- **`X`**: A row identifier.
- **`Scoring`**: A string indicating the name and date of the scoring session,  including details like the experiment's name, date, and subject identifier (e.g., "Conceptofseeing_2023_11_17_PW_Samira").
- **`Start`**: The start time of the observed behavior or event.
- **`Start_Frame`**: The frame number corresponding to the start of the behavior or event.
- **`Stop`**: The stop time of the behavior or event in seconds.
- **`Stop_Frame`**: The frame number corresponding to the stop of the behavior or event. 
- **`Subject`**: A string representing the name  of the subject (e.g., "Samira").
- **`Behaviour`**: The type of behavior or event being scored , i.e. "approach", "latency_first_choice", "choice", "food_taken", "phase".
- **`Value`**: The observed outcome or category of the `Behaviour` variable, i.e.  whether they approached the bowl or not (approach: "yes_approach" / "no_approach"), which bowl they chose (choice: "seen", "unseen"), the bowl of the first-approach latency (latency_first_choice: "visible" = seen bowl, "non_visible" = unseen bowl), and the duration of each phase (phase: "exploration", "pretest1a", "pretest1b", "pretest2", "test").
- **`phase`**: The experimental phase during which the behavior was recorded: "exploration", "pretest1a", "pretest1b", "pretest2", "test"  
- **`duration`**: The duration of the behavior or event, measured in seconds. Only applicable for some behaviors that were coded as durations.
- **`breed`**: The breed of the subject, such as "Yorkshire terrier".
- **`sex`**: The biological sex of the subject, represented as "M" for male or "F" for female.
- **`condition`**: The experimental condition ("cue", "control").
- **`start_side`**: The side at which the subject first found food in the initial exploration phase (L= unseen side, R= seen side).
- **`FCI_Group`**: Fédération Cynologique Internationale (FCI) classification of dog breeds into the following categories: "Companion/Toy", "Dachshund", "Pinscher/Schnauzer", "Pointing", "Retriever", "Scenthound", "Sheep/cattledog", "Sighthound", "Spitz/Primitive", "Terrier")
- **`FCI_Group1`**: A secondary classification of the `FCI_Group` variable recoding rare levels as "Other" (levels: "Herding", "Other", "Retriever", "Terrier", "Toy").
- **`birth_date`**: The birth date of the subject, formatted as `DD/MM/YYYY` (e.g., "04/05/2014"), allowing for the calculation of the subject's age at the time of the experiment.
- **`age`**: The subject's age in months at the time of the experiment. 
