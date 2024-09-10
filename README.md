# Yet Another SplendidGrandPiano SFZ

SFZ instrument that I made using public domain samples by AKAI. My goal was to create an instrument that works with LinuxSampler and has a number of interchangeable versions, including an extremely minimalistic one. Also it was also a good opportunity to learn about the SFZ format.

## Explanation :

|Bank/Instrument suffix|Velocity Layers|Mono/Stereo |Notes per sample |Total Number of Samples|
|:--------------------:|:------------:|:----------:|:---------------:|:---------------------:|
|**xs1 (ls)**          |1|mono       |3-4|30 |
|**xs2 (ls)**          |1|fake stereo|3-4|30 |
|**s1 (ls)**           |2|mono       |3-4|60 |
|**s2 (ls)**           |2|fake stereo|3-4|60 |
|**m1 (ls)**           |4|mono       |3-4|224|
|**m2 (ls)**           |4|fake stereo|3-4|224|
|**m3 (ls)**           |4|fake mono  |3-4|224|
|**m4 (ls)**           |4|stereo     |3-4|224|
|**l1 (ls)**           |4|mono       |1-3|452|
|**l2 (ls)**           |4|fake stereo|1-3|452|
|**l3 (ls)**           |4|fake mono  |1-3|452|
|**l4 (ls)**           |4|stereo     |1-3|452|

### Bank/Instrument

- Banks/instruments with **'ls'** are for LinuxSampler, while those without it are for any other software
- A bank/instrument without a number includes all banks with the same letter+number, which can be switched using the LSB CC32 command. For example, if the **'ya_splendid_grand_piano_l.sfz'** file is loaded, you can switch to **'l1'** by sending the LSB CC32 0 command, to **'l2'** by sending LSB CC32 1, and so on.

### Mono/Stereo

- **mono**: 1 sample, not panned (center).
- **fake stereo**: 1 sample, panned (lower notes to the left, higher notes to the right).
- **fake mono**: 2 samples, both not panned (center).
- **stereo**: 2 samples, panned (first sample 100% left, second sample 100% right).

### Notes per sample

The bank does not include samples for every note; some sounds are produced by changing the pitch of the samples. For example, '3-4' means that one sample is used to produce approximately 3-4 notes.