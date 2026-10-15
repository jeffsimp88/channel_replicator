# <center> Channel Replicator </center>
The Channel Replicator application will generate a .m3u playlist that will simulate a retro channel. It will include episodes, commercials, and bumpers. For best results, have episodes split up at the commercial breaks.
___
### How it Works
1. A list of shows, found in the TV Shows directory, will be shuffled, then starts at the beginning.
2. Picks a random season, then random episode of each show.
3. Finds the other segments of the show and puts them in order.
   * Anthology shows will randomly select three shorts, such as Looney Tunes.
4. Fills the commercial breaks with random selection of station and product commercials.
   * Holiday commercials are added based on the current date (i.e. Halloween or Christmas)
5. Adds intro and outro bumpers (i.e. `Comming up Next`, `Be Right Back`).
   * Depending on the channel, unique shorts will be added to breaks between shows.
6. It will complete these actions for each show, and will repeat the list of shows.

____
### Directory Layout
This application will choose the files on a specific directory tree.

Channel Replicator\
├── Bumpers\
│   ├── 1 - Coming Up Next\
│   ├── 2 - Station IDs\
│   ├── 3 - Pre- and Post-show bumper\
│   ├── 4 - Theme Songs\
│   ├── 5 - We_ll Be Right Back\
│   ├── 6 - Now Back To\
│   ├── Acme Hour and Looney Tunes Show Bumpers\
│   ├── CN Ads\
│   ├── CN Music Videos\
│   ├── CN Shorties\
├── Commercials\
├── Holiday Commercials\
│   ├── Christmas\
│   └── Halloween\
├── create_anthology_episode.py\
├── generate_commercials.py\
├── generate_episode.py\
├── generate_playlist.py\
├── playlist.m3u
___
### Video Formats
The preferred file formats for videos are:
- `.mp4`
- `.mkv`
- `.avi`

With episodes split at the commercial breaks, label them with `(a)` or `(1)` at the end of the file name.
Example:
- The Powerpuff Girls S01E01 (1).mp4
- The Powerpuff Girls S01E01 (2).mp4
- The Powerpuff Girls S01E01 (3).mp4

---
### How to Run
In the terminal:
```python generate_playlist.py```\
The message 'Your Playlist is ready!' will appear if no errors.