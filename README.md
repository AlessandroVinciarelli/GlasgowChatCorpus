The data can be downloaded at the following link:

<a href="https://www.dropbox.com/scl/fi/3smo02itebd0nceungnhm/Glasgow-Chat-Corpus.zip?rlkey=q7s6i612jlbviv4dtwwcoiy1f&dl=0">Glasgow Chat Corpus</a>

If you use the data, you are kindly invited to cite the following articles:

- A.Buker, G.Roffo and A.Vinciarelli, "Type Like a Man! Inferring gender from keystroke dynamics in live-chats", IEEE Intelligent Systems, Vol.34, No. 6, pp. 53-59, 2019 (DOI  10.1109/MIS.2019.2948514).
- A.Buker and A.Vinciarelli, "I Feel it in Your Fingers: Inference of Self-Assessed Personality Traits From Keystroke Dynamics in Interactive Dyadic Chats", Proceedings of the IEEE International Conference on Affective Computing and Intelligent Interactions, 2021 (DOI 10.1109/ACII52823.2021.9597389).
- A.Buker and A.Vinciarelli, "Who Is Typing? Automatic Gender Recognition from Interactive Textual Chats Using Typing Behaviour", in “Enabling Machine Learning Applications in Data Science. Algorithms for Intelligent Systems”, A.E.Hassanien, A.Darwish, S.M.Abd El-Kader, D.A.Alboaneen (eds.), Springer Verlag, pp. 3-15, 2021.

If you have any questions about the data, please contact Alessandro Vinciarelli (Alessandro.Vinciarelli@glasgow.ac.uk) or Abeer Buker (aabuker@iau.edu.sa).

---

The distribution includes three directories:

- chats: 60 csv files containing the keys pressed during the chats and their respective timestamps;
- personality: 60 csv files containing the answers given by the participants to the Big-Five Inventory 10;
- protocol: a K-fold protocol.




----

Directory "chats"


The naming convention of the files in directory "chats" is as follows: Cnn-QG.csv, where nn is an integer chat identifier between 1 and 30 with leading zero (e.g., 7 is written "07"), Q is a letter that stands for role ("C" for Caller and "R" for Receiver), and G is a letter that stands for gender ("F" for female and "M" for male).

For example, file C27-CM.csv contains the keys pressed by the caller (a male participant) in call 27, while file C27-RF.csv contains the keys pressed by the receiver in call 27 (a female participant).

The format of the files is as follows:

- column 1: the key that was pressed;
- column 2: the timestamp corresponding to the moment the key was pressed.

The files in directory "chats" have no header.

---

Directory "personality"

The naming convention of the files in directory "chats" is as follows: Cnn-QG-B5.csv, where nn is an integer chat identifier between 1 and 30 with leading zero (e.g., 7 is written "07"), Q is a letter that stands for role ("C" for Caller and "R" for Receiver), G is a letter that stands for gender ("F" for female and "M" for male), and "B5" stands for "Big-Five".

The format of the files is as follows:

Line 1 is the header and its format is as follows:

- columns 1 to 10: items 1 to 10 of the Big-Five Inventory 10 (the questionnaire for personality self-assessment administered to the participants)

Line 2 is the self-assessment of the participants corresponding to the file and its format is as follows:

- columns 1 to 10: each column is a score between 1 and 5 (1 means "strongly disagree", 2 means "disagree", 3 means "neither disagree nor agree", 4 means "agree" and 5 means "strongly agree"). Each score is the answer of the participants to the BFI-10 item of the corresponding column.

The scores can be mapped into personality self-assessments as follows (Sk is the score in column k, i.e., the answer of the participant to item k of the BFI-10):

Openness: S1-S6
Conscientiousness: S3-S8
Extraversion: S5-S10
Agreeableness:S9-S4
Neuroticism: S2-S7

---

Directory "protocol"

The format of the file in this directory is as follows:

- column 1: list of participants in fold 1;
- column 2: list of participants in fold 2;
- column 3: list of participants in fold 3;
- column 4: list of participants in fold 4.

The protocol is provided for reproducibility purposes. By using the same folds, corpus users can replicate the experiments performed by others.
