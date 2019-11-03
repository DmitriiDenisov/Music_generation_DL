# Music_generation_DL

### Current status:
Generating notes only with LSTM


### TODO:

1. [ ] Look through `mlp_gan.py`
2. [ ] Apply `mlp_gan.py` to one of our basic examples in order to understand how they form training dataset 
3. [ ] Once we finished with 2 => understand if this method is suits us or not
 
4. [ ] Write a class/function for data preprocessing (reading midi file, scaler etc)
5. [ ] Training and prediction features must include Velocity, Time, Message Type; and not only note value.
6. [ ] Reuse the generated information when creating a new file.


### Notes
- Time is captured in delta time, i.e. difference in time between the current note, and the one before it
- Default value for 1 beat is 96 clocks, time is measured in clocks when viewed with `mid.print_tracks()`, and as a fraction of a beat when viewed with `msg.time` (or `msg.dict()`).
- We can use `mid.print_tracks()` to get a quick overview of the MIDI file
