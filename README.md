# Voice Kit False Positive Detector

Simple extension of microWakeWord that uploads a few seconds of audio before each wake word detection. These are false positives if you never purposefully speak the wake word.

## Installation

1. Install the companion add-on [![Show add-on](https://my.home-assistant.io/badges/supervisor_addon.svg)](https://my.home-assistant.io/redirect/supervisor_addon/?addon=47701997_voicekit_fpc&repository_url=https%3A%2F%2Fgithub.com%2Frhasspy%2Fhassio-addons)
2. Modify the `voicekit_fpc.yaml` file and set `<HA IP ADDRESS>` to the IP address of your Home Assistant machine 
3. Flash the ESPHome YAML to the VoiceKit


## Usage

Every time you speak the wake word ("ok nabu"), the VoiceKit should turn on the LEDs and upload audio to the server.

In Home Assistant, check the `/share/voicekit-fpc` directory for WAVE files.


## Advanced

Instead of using the HA add-on, you can just run `server.py` anywhere that has Python available. WAVE files will be saved in the current directory. See `python3 server.py --help` for more options.
