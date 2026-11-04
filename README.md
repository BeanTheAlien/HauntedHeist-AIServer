# HauntedHeist-AIServer
The server used for AIs by Haunted Heist.

Visit the main Haunted Heist repo [here](https://github.com/BeanTheAlien/HauntedHeist).

# AIs & Implementation Notes
## Audio Synthesis / Text-to-Speech
Audio synthesis (commonly text-to-speech (TTS)) is used to formulate *predicted* audio lines from a player, in the event that they have died to a ME.\
The TTS pipeline uses [audio.cpp](https://github.com/0xShug0/audio.cpp) and Kokoro
