# HauntedHeist-AIServer
The server used for AIs by Haunted Heist.

Visit the main Haunted Heist repo [here](https://github.com/BeanTheAlien/HauntedHeist).

# AIs & Implementation Notes
## Audio Synthesis / Text-to-Speech
Audio synthesis (commonly text-to-speech (TTS)) is used to formulate *predicted* audio lines from a player, in the event that they have died to a ME.\
The TTS pipeline uses [audio.cpp](https://github.com/0xShug0/audio.cpp) and [Kokoro (82M parameters)](https://huggingface.co/hexgrad/Kokoro-82M).
## Automatic Speech Recognition / Speech-to-Text
Automatic speech recognition (commonly speech-to-text (STT)) is used to process and transcribe the content of an audio file (in this case, what players speak).\
In each session, everything that a player says (during any time they are alive) is recorded into WAV files, which are then processed and used to "guess" what a player *might* realistically say.\
The STT pipeline uses [Faster-Whisper (Large v3)](https://huggingface.co/Systran/faster-whisper-large-v3).
## Advanced Reasoning
Advanced reasoning is used to predict what a player is most likely to say, given a prompt or idle conversation.\
Additionally, advanced reasoning is used to give ghosts instructions for actions, when no action can be determined (rare edge case).\
The advanced reasoning pipeline uses [Calme 3.2 Instruct (72B parameters)](https://huggingface.co/MaziyarPanahi/calme-3.2-instruct-78b).
