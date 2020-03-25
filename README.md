# LiveCode-iOS-TextToSpeech-Extension
An extension for LiveCode that enables Text-To-Speech functionality on iOS.

# Documentation

```EdHSpeak(in pRate as CFloat, in pPitch as CFloat,in pVolume as CFloat,in pVoice as String, in pString as String) returns String```

- reads a text given as argument (*pString*), with as additional parameters the voice, the rate, the pitch and the volume. Returns "Done" as a String if everything went smoothly.
    - Rate between 0 and 1
    - Pitch between 0.5 and 2
    - Volume between 0 and 1
    - Voice (one of the voices in the list returned by getVoices() or language and locale like "fr-FR")

```EdHGetVoicesList()```
- returns a list of Strings that contains the available voices' names. Returns an empty list if something went wrong.

```EdHGetVoices()```
- returns all available voices but in one unique semicolon separated string.

```EdHPause(in tWord as CFloat)```
- pauses the current reading.
    - tWord 0 or 1 : 0 is to stop immediately, 1 to stop at the end of the word

```EdHStop(in tWord as CFloat)```
- stop the current reading.
    - tWord 0 or 1 : 0 is to stop immediately, 1 to stop at the end of the word

```EdHContinue()```
- resume a current paused reading.

```EdHIsSpeaking()```
- returns true if a reading is ongoing (even paused) as a Bool false elsewhere.

```EdHIsPaused()```
- returns true if a reading is paused, false elsewhere (as a Bool).