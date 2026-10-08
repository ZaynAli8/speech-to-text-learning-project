# Speech-to-text learning project

A **tutorial-guided, work-in-progress** notebook that transcribes a locally supplied audio file with the pretrained `facebook/wav2vec2-base-960h` model. The project demonstrates audio loading and resampling, model inference, and decoding token predictions into text. It does not train a model or report an accuracy benchmark.

## What I did

- Loaded audio with `librosa` and resampled it to 16 kHz.
- Used Hugging Face's `Wav2Vec2Processor` and `Wav2Vec2ForCTC` with PyTorch to run speech-recognition inference.
- Selected predicted tokens from model logits and decoded them into a transcription.

**Outcome:** a local notebook workflow that prints a transcript for an audio file supplied by the user. The notebook is intentionally published without audio, saved outputs, or credentials.

## Run locally

1. Create a Python virtual environment and install `requirements.txt`.
2. Put your own `sample_audio.wav` beside the notebook. Use audio you have permission to process.
3. Open `speech_to_text.ipynb` in Jupyter or VS Code and run the cells in order. The first model load downloads pretrained weights from Hugging Face.

This was a learning exercise following a Simplilearn speech-to-text tutorial. The notebook has been reorganized and cleaned to make each step readable; performance on a particular recording has not been benchmarked.
