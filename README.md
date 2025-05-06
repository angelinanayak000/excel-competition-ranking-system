# Excel-competition-ranking-system
A Microsoft Excel project implementing a weighted scoring model and automated ranking using the RANK.EQ function for the IMPULSE – “Next Big Idea” competition. This system evaluated 11 student teams based on criteria like problem, solution, business model, market, and presentation, as judged by five experts.

# Idea Pitch Competition Score Sheet and Ranking System

![Screenshot 2025-05-06 194839](https://github.com/user-attachments/assets/87bac28b-6240-4b65-801c-05133a5c9c01)


## Overview

This project details the creation and implementation of a structured scoring and ranking system developed for the IMPULSE – “Next Big Idea” competition, a key event of the **IMPULSE One Day Startup Conclave** held at the Institute of Agricultural Sciences (IAS), Siksha 'O' Anusandhan (Deemed to be University), Bhubaneswar, India, on **April 29th, 2025**. The competition, organized by the Incubation Centre at Siksha 'O' Anusandhan (Deemed to be University) in collaboration with Startup Odisha, AIC CII, and AIC-SOA Foundation, aimed to foster the innovative spirit of student entrepreneurs. The system efficiently evaluated 11 participating student teams based on their 10-minute pitches, utilizing the expert judgment of five esteemed judges. The project leverages Microsoft Excel to calculate weighted scores based on predefined criteria, determine participant rankings using the `RANK.EQ` formula, and ultimately identify the Winner and Runner-Up of the competition.

## Key Features

* **Structured Evaluation Criteria:** Implemented a scoring framework based on five main criteria: Problem/Opportunity (30%), Solution/Idea (40%), Business Model (10%), Market Opportunity (10%), and Team & Presentation (10%). Each main criterion included weighted sub-criteria for more granular evaluation.
* **Weighted Scoring System:** Developed a method to calculate a weighted total score for each judge's evaluation of each team, taking into account the varying importance of the sub-criteria.
* **Averaged Judge Scores:** Calculated an "Average Final Score" for each team by averaging the total scores awarded by the five judges, providing a consolidated measure of their performance.
* **Automated Ranking with `RANK.EQ`:** Utilized Excel's `RANK.EQ` formula to automatically determine the rank of each team based on their average final score, ensuring an objective and data-driven outcome.
* **Clear Identification of Top Performers:** The ranking system directly facilitated the identification and declaration of the Winner (Rank 1) and the Runner-Up (Rank 2) of the competition.
* **Organized Data Management:** The Excel sheet was structured for efficient data entry of judge scores and clear presentation of calculated scores and rankings.

## Technologies Used

* **Microsoft Excel:** The primary tool used for creating the score sheet, implementing formulas for weighted scoring and ranking, and managing the competition data.
* **Gemini (AI Assistant):** Utilized as an AI assistant during the development of this project, potentially for brainstorming, refining the structure, or assisting with the clarity of the evaluation criteria.

## How It Works

1.  **Defined Evaluation Framework:** The competition utilized a structured evaluation framework with five main criteria, each having specific weightings and further broken down into sub-criteria with their own weight percentages. Judges were instructed to score each sub-criterion on a scale of 1 (Poor) to 5 (Excellent). The detailed breakdown of criteria and sub-criteria with their weights is as follows:
**Score Sheet**
![image](https://github.com/user-attachments/assets/f4f9c644-add7-48f7-a89f-58222d45d206)

    * **Problem/Opportunity (30%)**:
        * Significance and market size of the problem (20%)
        * Validation of the problem (research, data) (10%)
    * **Solution/Idea (40%)**:
        * Uniqueness and innovation of the solution (25%)
        * Feasibility and practicality of the solution (15%)
    * **Business Model (10%)**:
        * Clarity of the revenue model (10%)
    * **Market Opportunity (10%)**:
        * Understanding of the target market (10%)
    * **Team & Presentation (10%)**:
        * Clarity and organization of the presentation (5%)
        * Effective time management (within 10 minutes) (5%)

3.  **Weighted Judge Score Calculation:** For each team, each judge's overall score was calculated as a weighted sum of their scores for the individual sub-criteria. The following Excel formula was used:

    ```excel
    =($D$6*E6)+($D$7*E7)+($D$9*E9)+($D$10*E10)+($D$12*E12)+($D$14*E14)+($D$16*E16)+($D$17*E17)
    ```

    * `$D$6`, `$D$7`, etc.: Absolute references to the cells containing the pre-defined weights for each sub-criterion.
    * `E6`, `E7`, etc.: Relative references to the cells containing the individual judge's score (1-5) for each sub-criterion.
    **A Team Score Sheet**
    ![Screenshot 2025-05-06 194911](https://github.com/user-attachments/assets/fc274c54-02e1-47d9-bddd-99278ffe368a)


4.  **Average Final Score Determination:** To obtain a consolidated score for each team, the "Average Final Score" was calculated by taking the arithmetic mean of the total scores awarded by the five judges. The Excel formula used was:

    ```excel
    =AVERAGE(C2:G2)
    ```

    * `C2:G2`: Range of cells containing the total scores given by Judge 1 to Judge 5 for a specific team.

5.  **Automated Team Ranking:** The final ranking of the teams was determined using the `RANK.EQ` function in Excel, applied to the "Average Final Score" of all 11 participating teams. The formula used was:

    ```excel
    =RANK.EQ(H2,H:H,0)
    ```

    * `H2`: Cell containing the "Average Final Score" for a specific team.
    * `H:H`: The entire column containing the "Average Final Scores" of all 11 teams.
    * `0`: Specifies that the ranking should be in descending order, with the highest average score receiving a rank of 1.
    **FInal Score Sheet of 11 Teams with Rankings**
    ![Screenshot 2025-05-06 194839](https://github.com/user-attachments/assets/33931f72-076a-4e30-a975-d0e9fff6c3ed)


6.  **Winner and Runner-Up Identification:** Based on the final rankings, the team holding Rank 1 ("AAHAR AI") was declared the Winner of the IMPULSE – “Next Big Idea” competition, and the team with Rank 2 ("AGRO FAST - SMART BLOOM") was recognized as the Runner-Up.


## Challenges and Solutions

* **Ensuring Consistency in Judge Scoring:** One of the key challenges was ensuring a degree of consistency in scoring across the five judges, given their potentially varied perspectives. This was addressed by providing clear and detailed guidelines for each criterion and sub-criterion, along with appropriate anchoring descriptions for each point on the 1-5 scoring scale. This helped to align the judges' understanding of the evaluation metrics.
* **Managing Data Entry:** Efficiently managing the data entry for the scores from five judges across 11 teams required a well-organized spreadsheet structure with clear labeling.
* **Presenting Results Clearly:** The final ranking and the identification of the Winner and Runner-Up needed to be presented in a clear and easily understandable format within the Excel sheet.

## Lessons Learned

* The importance of a well-defined and weighted evaluation system, coupled with clear scoring guidelines, for ensuring fairness and consistency in competitive judging.
* The efficiency and versatility of spreadsheet software like Excel for handling complex calculations, data organization, and automated ranking in real-world scenarios.
* The significance of proactive measures, such as providing anchoring guidelines, to mitigate potential inconsistencies in subjective evaluations.

