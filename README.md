# music-catalog
Populates a SQLite database with information parsed from audio files/tags for easier music library management. Supports conditional CSV exports.

Currently stores the following data:

- Artist
- Album Artist
- Year
- Album
- Track Number
- Song Title
- Bitrate
- Sample Frequency
- Genre
- Duration (seconds)
- File Path
- Directory
- Insert Timestamp
- BLAKE2B Hash

## Usage
~~~
python3 music-catalog.py ~/path_to_music
~~~
To view this README invoke with `--help`

## CSV Export
Currently supports four export formats:

- (f)ull: 	    Export all music info to csv
- (a)lbums: 	Export album info to csv
- (b)itrate: 	Export conditionally by bitrate
- (m)issing: 	Export files with missing tag data

Bitrate exports are determined using operators `=, <, >, <=, >=`

## Storage

The database resides at `data/music_library.db`.

Timestamped CSV exports are stored in `data/csv_exports`

## To-Do
- Blob image data?
- Add tagging functionality w/Discogs API
