# DeepFake

**DeepFake project for M2 NLP**

The project aims to create a multilingual corpus of deepfake audios using 5 different vocoders () and two TTS models (). The following paragraph will provide the benefits of this project whilst the bottom paragraph will provide instructions to access the audios and install the libraries. 

# Benefits of a multilingual DeepFake corpus

Creating a multilingual deepfake audio corpus has several potential benefits, although it's important to note that deepfake technology raises ethical concerns, and it's essential to use such technology responsibly. Our corpus is constructed with an intention of training systems for deepfake detection. Here are some potential benefits:

**Diversity and Generalization:**
A multilingual corpus allows the training of deepfake models on a diverse set of languages, dialects, and accents. This diversity can help the model generalize better to various linguistic nuances and improve its performance across different linguistic contexts. In our instance, we are using four languages that as we believe provide satisfactory linguistic variation: dutch, french, spanish and german. 

**Robustness and Adaptability:**
Exposure to a wide range of languages enhances the robustness of deepfake models. These models may become more adaptable to different linguistic environments, making them less prone to bias and more effective in handling variations in speech.

**Transfer Learning:**
Training a deepfake model on a multilingual corpus may facilitate transfer learning. The knowledge gained from one language can be transferred to improve the model's performance when dealing with a new language. This can reduce the amount of data needed for training in a new language.

**Improved Accessibility and Inclusivity:**
A multilingual corpus allows for the development of deepfake technology that supports and understands a broader range of languages. This can contribute to increased accessibility and inclusivity in voice-related technologies, benefiting users from different linguistic backgrounds.

**Applications in Language Learning:**
A multilingual deepfake audio corpus can be used in language learning applications to provide learners with diverse examples of native speakers, helping them practice and improve their language skills.

While there are potential benefits, it's crucial to consider and address ethical concerns, including issues related to consent, privacy, misinformation, and potential misuse of the technology.

# Instructions

| Current Stage         | Next Stage              |
| ----------------------| ----------------------- |
| Vocoder Training      | Tacotron Training       |

Progress, trial audios and graphs can be found here: https://drive.google.com/drive/folders/1N7ZZv8_XB92UpVr9Sb_4a1986dToDqaa?usp=sharing

## Library installation:

The project uses TTS library. The installation instructions are provided below:

You can install from PyPI as follows:

```python
pip install TTS  # from PyPI
pip install git+https://github.com/coqui-ai/TTS  # from Github
```
Installing from source for development: 

```python
git clone https://github.com/coqui-ai/TTS/
cd TTS
make system-deps  # only on Linux systems.
make install
```
Developer friendly installation

```python
$ git clone https://github.com/coqui-ai/TTS
$ cd TTS
$ pip install -e .
```
You can read more about the library and check the documentation here: https://github.com/coqui-ai/TTS/ 

It is important to note that the formatter has to be adapted to your custom dataset after the installation. Our adaptation instructions are provided in a separate folder.

## Present files and folders: 

| **Folder**          | **Description**        |
| --------------------| -----------------------|
| Formatter           | custom formatter code  |
| Vocoders            | vocoder training codes |
| TTS systems         | tts training codes     |
| Errors              | error documentation    |
| Final report        | final report and slides|
| requirements.txt    | all packeges in our env|


## Datasets
CML-Multi-Lingual-TTS is a Text-to-Speech (TTS) dataset developed at the Center of Excellence in Artificial Intelligence (CEIA) of the Federal University of Goias (UFG). This dataset is based on Multilingual LibriSpeech (MLS) for training TTS models, consisting of audiobooks in seven languages: Dutch, French, German, Italian, Portuguese, Polish, and Spanish. Their purpose in creating this dataset was to giveway to new research possibilities in the TTS area for multi-lingual models. 

Through these links you can access to the datasets and related information.
https://www.fredso.com.br/CML-TTS-Dataset/
https://github.com/freds0/CML-TTS-Dataset
