# Speech-Emotion-Recognition-CS-5530
This is an attempt to accurately classify the emotion of a speaker in (near) realtime. The Jupyter notebook outlines each step of the process including EDA, data sourcing, cleaning, feature engineering, modeling, evaluation, and web interface deployment.

**Devlog 3/20/2025: Feature engineering / refinement**
As you can see from the following confusion matricies, the current performance is pretty mediocre.
"strong/normal" features of each emotion are plotted adjacent to eachother for easier comparison. 

Ideally, we'd like to see see high numbers about the diagonal with very little "bleedover" into adjacent cells.
- Adjacent cells similar in saturation indicate the model is struggling with decerning strong from normal affect.
- There is also a strong bias in the model towards "sad".
<img width="2526" height="2497" alt="joint_confusion_matrix" src="https://github.com/user-attachments/assets/a0c6d68e-8f1a-476e-9655-bdb7212b397d" />
<img width="1513" height="1538" alt="emotion_confusion_matrix" src="https://github.com/user-attachments/assets/c4af6b66-d1a0-43be-ac5e-b4dfc1a7ea80" />

- The following graphic issustrates the overlap of sadness from the current features extracted.
<img width="1690" height="690" alt="overlap" src="https://github.com/user-attachments/assets/ff77610a-22d4-495c-8b2e-fdb174033aa2" />
Goal: Look into methods to improve sadness accuracy
