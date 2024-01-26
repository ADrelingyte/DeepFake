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

## Training

Sample command after adjusting the parameters to fit your dataset:

```python
$ CUDA_VISIBLE_DEVICES="0" python train_wavegrad.py
```
Training on multiple GPUs:

```python
$ CUDA_VISIBLE_DEVICES="0, 1, 2" python -m trainer.distribute --script <path_to_your_script>/train_wavegrad.py
```
Continuing training and saving checkpoints:

```python
python -m trainer.distribute --script <path_to_your_script>/train_wavegrad.py --gpus 0,1,2,3 python -m trainer.train_tts --restore_path <path_to_your_checkpoint>/train_wavegrad.py/checkpoint_xxx.pth"
```

Tesorboard or inference_vocoder.py can be used to synthesized audios after the training.
Tensorboard should be used in the output directory:

```python
tensorboard --logdir .
```

## Datasets
CML-Multi-Lingual-TTS is a Text-to-Speech (TTS) dataset developed at the Center of Excellence in Artificial Intelligence (CEIA) of the Federal University of Goias (UFG). This dataset is based on Multilingual LibriSpeech (MLS) for training TTS models, consisting of audiobooks in seven languages: Dutch, French, German, Italian, Portuguese, Polish, and Spanish. Their purpose in creating this dataset was to giveway to new research possibilities in the TTS area for multi-lingual 
