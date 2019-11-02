# Music_generation_DL

### Current status:
Generating notes only with LSTM


### TODO:

1. Write a class/function for data preprocessing (reading midi file, scaler etc)
2. Training and prediction features must include Velocity, Time, Message Type; and not only note value.
3. Reuse the generated information when creating a new file.


### Notes
- Time is captured in delta time, i.e. difference in time between the current note, and the one before it
- Default value for 1 beat is 96 clocks, time is measured in clocks when viewed with `mid.print_tracks()`, and as a fraction of a beat when viewed with `msg.time` (or `msg.dict()`).
- We can use `mid.print_tracks()` to get a quick overview of the MIDI file
