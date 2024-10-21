
---

# Integrated Diagnostic System Based on AI and Signal Processing for Identifying Articulation Disorders and Retrieval Difficulties in Children Transitioning to First Grade

### Project Overview
This project is an AI and signal-processing-based system designed to identify articulation disorders and retrieval difficulties in children transitioning to first grade. The goal of the project is to provide an initial diagnostic tool intended for home use, which reduces the need for initial consultations with a speech therapist, saving time and money. Additionally, the system is designed to provide children with comfort by operating in a familiar environment and offering speech therapists detailed preliminary information about the child's speech, enabling comparisons between manual assessments and system-generated results.

### Key Features
![image](https://github.com/user-attachments/assets/51b73b4a-c91a-4575-b036-28efa871e2cf)
![image](https://github.com/user-attachments/assets/0bf0d7ca-6c5b-4850-9864-6ed2c11de52d)

1. **Automatic Speech Analysis**: The system utilizes AI and signal processing to analyze voice recordings of children saying specific words and identifies articulation errors.
2. **User-Friendly Interface**: The interface allows users (parents, speech therapists) to easily interact with the system and view the analysis results.
3. **Spectrogram Display**: Each analyzed word is displayed with a spectrogram showing the phoneme identification, retrieval time, and position within the word.
4. **Preliminary Diagnostic Tool**: Speech therapists can use the system's data as a first-stage diagnostic, helping them prepare more efficiently for future therapy sessions.

### Flask Application Development
As part of the project, we developed a web application using **Flask**, a lightweight web framework for Python. The application serves as an interactive interface that allows users (both children and parents) to engage with the system in a simple, accessible way. Here's what the application does:

1. **Interactive User Flow**: 
   - The application presents images from a standardized set of objects, which the child is prompted to name. 
   - Once the image is displayed, the app automatically starts recording the child's speech and measures the response time from when the recording begins until the child speaks.
   
2. **Real-Time Feedback**:
![image](https://github.com/user-attachments/assets/09d6a125-8b4f-46cc-9b5f-8fda3beaabd6)
![image](https://github.com/user-attachments/assets/b5f0aa23-b4db-4ace-975f-8690ff197549)

   
   - After each session, the system processes the recording, identifies the phonemes, and displays a spectrogram with detailed information about the errors detected, if any.
   - Users can replay the recordings, review the results, and analyze the articulation errors using the spectrogram provided.

4. **Result Saving and Management**:
   - Users can choose where the results (audio recordings and analysis images) are saved on their computer, making it easier to organize the session data for later use by speech therapists or parents.
   
5. **Standalone Application**: The Flask app is designed to be packaged as a standalone executable file (.EXE), ensuring that it can be run on any computer without needing to install additional software dependencies or Python environments.

The application’s simple and intuitive interface makes it user-friendly for parents, children, and professionals alike, allowing speech therapists to easily monitor and track progress over time.

### Methodology
![image](https://github.com/user-attachments/assets/1c4e7817-b13c-41c2-9a5d-9dd14ba0dbce)
The methodology developed in this project incorporates advanced machine learning techniques and signal processing. The system is built on top of the **Allosaurus** library, a multilingual allophone-based acoustic model for phoneme recognition, which has been adapted specifically for Hebrew phoneme identification. Allosaurus is known for its versatility and high accuracy across different languages, making it a suitable choice for this project. You can find more about Allosaurus on its [GitHub page](https://github.com/xinjli/allosaurus) or in the original research paper: *"Universal Phone Recognition with a Multilingual Allophone System" by Xinjian Li et al. (2020)*.

- **Data Collection**: Voice recordings of children were collected and used to train and validate the model.
- **Signal Processing**: The recorded speech is processed to identify phonemes, and specific algorithms are applied to handle different speech conditions and background noise.

### Algorithms Used
Several key algorithms were employed in the system to ensure accurate recognition of phonemes and efficient handling of audio data:

1. **Voice Activity Detection (VAD)**: This algorithm detects segments of speech within an audio recording by analyzing the short-term energy (STE) and zero-crossing rate (ZCR) of the signal, allowing the system to filter out non-speech parts and focus on relevant audio.
   
2. **Mel-Frequency Cepstral Coefficients (MFCCs)**: This technique is used to extract features from the speech signal by representing the sound spectrum in a way that aligns with human auditory perception. MFCCs help capture important frequency components for phoneme recognition.
   
3. **Connectionist Temporal Classification (CTC)**: CTC is used to map the variable-length input audio features to the corresponding phoneme sequence without requiring perfect alignment between the audio and the phonemes. This is essential for handling the dynamic nature of spoken language.
   
4. **Beam Search Decoding**: The system uses beam search to efficiently decode the best possible sequence of phonemes from the probabilistic predictions of the model, improving the overall accuracy of the recognition process.

### Goals and Objectives
- Develop a robust, AI-based diagnostic tool for early detection of articulation disorders.
- Reduce the need for repeated visits to speech therapists by providing initial assessments that can be reviewed in a home setting.
- Present a graphical representation of the identified phonemes, including retrieval time and error categorization (semantic or phonological).

### Results
![image](https://github.com/user-attachments/assets/43d50d34-5da0-4c19-af82-357b17869b7d)
![image](https://github.com/user-attachments/assets/7a774a55-94fe-4abb-9ca0-0448016917cc)
![image](https://github.com/user-attachments/assets/b48e2e35-879e-4135-9ddb-aa51abc15681)


The system successfully identifies phonemes with a high degree of accuracy, making it a useful tool for both parents and speech therapists to detect potential speech impairments. However, challenges with the quality of recordings affected the overall performance, indicating room for improvement in future iterations.

### Future Work
The system can be expanded to support additional languages, improve recording quality by integrating advanced equipment, and add features like expression and intonation analysis. Future work may also focus on deploying the system in educational or mobile app formats to increase accessibility.

---

