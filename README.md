# Music_generation_DL

### Current status:
Generating notes only with LSTM

### Вопросы
1. Почему миди содержит два трека?
2. Как влияет нормализация случайного вектора?

### Ideas:
- Present Music as a matrix ```M``` : `96 x time` where 96 is the total number of notes. Cell `M_ij` is equal to `1` if not `i` at time `j` is on. Otherwise is it `0`. 
- Cut this Matrix `M` on blocks `96 x 96`
Source: https://github.com/HackerPoet/Composer

### TODO:

- [ ] Once again remember how data stores in midi
- [ ] Read theoretical material on topic in order to understand how to predict simultaneously several time series
- [ ] Examine some simple options on github/
- [ ] Look through `mlp_gan.py`
- [ ] Apply `mlp_gan.py` to one of our basic examples in order to understand how they form training dataset 
- [ ] Once we finished with 2 => understand if this method is suits us or not
 
- [ ] Write a class/function for data preprocessing (reading midi file, scaler etc)
- [ ] Training and prediction features must include Velocity, Time, Message Type; and not only note value.
- [ ] Reuse the generated information when creating a new file.


### Notes
- Time is captured in delta time, i.e. difference in time between the current note, and the one before it
- Default value for 1 beat is 96 clocks, time is measured in clocks when viewed with `mid.print_tracks()`, and as a fraction of a beat when viewed with `msg.time` (or `msg.dict()`).
- We can use `mid.print_tracks()` to get a quick overview of the MIDI file
