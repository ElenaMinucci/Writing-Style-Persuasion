# Data Log 
The contents of the `data.csv` file are organised as follows:
* **index**: Observation index.
* **receiverID**: Receiver ID who rated the statement in that observation.
* **persuaderID**: Persuader ID who wrote the statement for that observation.
* **statementID**: the statement ID for that observation, which was written by the persuader on the same observation row and evaluated by the receiver on the same observation row.
* **BFI1_receiver:BFI44_receiver**: Answers to the 44-items Big Five Inventory Questionnaire, completed by the receiver of that observation.
* **BFI1_statement:BFI44_statement**: Answers to the 44-items Big Five Inventory Questionnaire, completed by the persuader who wrote the statement in that observation.
* **extraversion_receiver:openness_receiver**: The Big Five scores of the receiver in that observation, averaged from the relevant BFI items.
* **extraversion_statement:openness_statement**: The Big Five scores of the persuader who wrote the statement in that observation, averaged from the relevant BFI items.
* **gender_receiver, age_receiver, educationlevel_receiver**: Gender, age and education level of the receiver in that observation.
* **gender_statement, age_statement, educationlevel_statement**: Gender, age and education level of the persuader who wrote the statement in that observation.
* **Greg_prompt_1:Greg_prompt_11**: The content of each textbox in the receiver's writing task, which was then concatenated to make **receiver_text_combined**. To see the textbox contents for the persuader's writing task too, please refer to the Pers-Pers Dataset repository: https://github.com/ElenaMinucci/Pers-Pers-Dataset
* **receiver_text_combined**: The full text written by the receiver in that observation.
* **statement_text_combined**: The full statement written by the persuader in that observation.
* **topic**: the prompt used for the statement in that observation. Each prompt is about a different character (Abi, Claudia, Matthew, Susan). For the complete prompts, see the `prompts.md` file in https://github.com/ElenaMinucci/Pers-Pers-Dataset
* **display_order**: order in which the statements were rated by receivers given randomisation. Receivers evaluated 5 statements x 4 topics (20 observations per receiver, Abi1 to Susan5). This column is used to preserve the Perceived Persuasiveness Scale (PPS) scores for each observation given randomisation.
* **Abi1_pps1:Susan5_pps9**: Scores of the PPS, which receivers used to evaluate the persuasiveness of each statement they observed. The first part of these column names contains display order (e.g., Abi1, while the second part (pps[1-9]) contains the item number on the PPS scale. For example, Abi5_pps1 refers to the score on item 1 of the PPS on the fifth randomly drawn statement about Abi seen by that receiver.
* **Segment_statement:Emoji_statement**: Linguistic features of the statement's writing in that observation, extracted from the LIWC software.
* **Segment_receiver:Emoji_receiver**: Linguistic features of the receiver's writing in that observation, extracted from the LIWC software.
* **Questions_receiver:alternatives_receiver**: Content features of the receiver's writing in that observation.
* **Questions_statement:alternatives_statement**: Content features of the statement's writing in that observation.
* **persuasion_score**: Persuasion score for that observation, obtained by averaging across the nine PPS items for that observation.
