# Offline Smart Voice Assistant (STT & TTS)

A Kaggle‐notebook demo of a free, self-contained voice assistant that uses:

- **VOSK** for offline Speech-to-Text  
- **DialoGPT-small** for on-device chat responses  
- **gTTS** for Text-to-Speech  
- **pydub** & **soundfile** for audio I/O  

No paid APIs or internet access required once models are downloaded.

---

## Quick Start

1. **Clone & open** this notebook on Kaggle.  
2. **Run the “Install & Download” cell** to install packages and fetch the VOSK model.  
3. **Generate or upload** a short WAV file named `sample_input.wav` (mono, 16 kHz).  
   - To auto-generate: run the “Generate sample question” cell.  
   - Or click **Upload → sample_input.wav** in the sidebar.  
4. **Run the “STT → LLM → TTS” cell**. It will:  
   1. Transcribe `sample_input.wav` offline via VOSK  
   2. Generate a smart reply with DialoGPT-small (in-notebook)  
   3. Synthesize `reply.wav` via gTTS  
   4. Embed and play both clips inline  
5. **Listen**: click the audio players under “Question” and “Answer.”

---

## Usage Details

- **STT**: VOSK small English model (downloaded once).  
- **LLM**: `microsoft/DialoGPT-small` loaded via HuggingFace Transformers.  
- **TTS**: Google’s free gTTS service.  
- **Audio handling**: `soundfile` & `pydub` convert between WAV/MP3 and resample.

No external API keys needed.

---

## Demo Recording

- Use **OBS Studio** (or similar) to record your notebook session:  
  1. model download & setup  
  2. generation of `sample_input.wav`  
  3. STT, response generation, TTS, and audio playback  

