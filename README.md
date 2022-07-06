FPV telemetry overlay for Ardupilot/Betaflight

# Convert ardupilot/betaflight telemetry log to SSA/SRT subtitles

## Export subtitles in SSA format (better positioning on the screen) and SRT (for video players that do not support SSA)

![MPV screenshot](img/mpv-shot0005.jpg?raw=true "MPV screenshot")

# Install

## Install Anaconda
[Download Anaconda](https://www.anaconda.com)

Products -> Anaconda Distribution

All settings default

### run "Anaconda Powershell Prompt"
```
pip install geopy
cd <project folder>
jupyter notebook .\TelemetryOverlay.ipynb
```

## config.yaml
```
log:
  # betaflight / ardupilot
  type: betaflight
  file: c:/Dropbox/Projects/FPV/_Logs/Taranis/Titan-2021-07-25.csv
output-dir: c:/Projects/FPV/_Video/2021-07-25_Titan@/
video-files:
  # filename: length in sec
  GH010372.MP4: 531
  GH020372.MP4: 77
shift-sec: 51
```

### Log columns

|Column  |Ardupilot|Betaflight|Calc|
|--------|---------|----------|----|
|time    |    +    |    +     |    |
|lat     |    +    |    +     |    |
|lon     |    +    |    +     |    |
|alt     |    +    |    +     |    |
|0420    |         |    +     | +  |
|RSSI(dB)|    +    |    +     |    |
|air_spd |    +    |          |    |
|spd     |         |    +     |    |
|sats    |         |    +     |    |
|bat	 |    +    |    +     |    |
|curr    |    +    |    +     |    |
|mah	 |         |    +     |    |
|thr     |    +    |    +     |    |
|ARM     |    +    |          |    |
|gps_spd |         |          | +  |
|curr_avg|         |          | +  |
|eff     |         |          | +  |