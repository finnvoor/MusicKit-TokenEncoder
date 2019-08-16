# MusicKit-TokenEncoder
---
A simple script to convert your MusicKit key into a token that can be used in shortcuts

### Usage
1. Install the JWT gem by opening terminal and typing 
`sudo gem install jwt`
2. Run the script by dragging it into terminal and then passing the .p8 file, your Key ID, and your Team ID (example: `./../../TokenEncoder ‘/../AuthKey_xxx.p8’ KEYID123 TEAMID124`).  You can do this by dragging the script into terminal, then dragging the .p8 file into terminal, then typing your Key ID followed by a space and your Team ID. After pressing return the script should output a 206 character token in the form of xxxxx.yyyyy.zzzzz. This is your final JWT token that will be used as authentication when making requests to the MusicKit API.
