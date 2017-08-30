# alias_mpg321
Quick alias-like tools for playing music from the command line that wrap and/or configure mpg321 to make it more user-friendly as a general music player. Mpg321 isn't a perfect music player (it doesn't handle every format I'd like), but it can certainly do enough of what I need without the extra load of GUI-based music players.

I've tried to keep the mpg321_aliases file fairly self-explanatory. If you want to contribute a function or alias, please make it similarly clear - not necessarily commented, but beautiful.[1](https://en.wikipedia.org/wiki/Are_You_Experienced%3F_(song))

To start with, I added aliases for some of the hackier tricks I'd seen online to change mpg321's behavior with one-liners. I've also begun working on tools to quickly find mp3 files and generate playlists. I'd like this to eventually be a full replacement for GUI-based music players. I don't want your streaming services - you can pry my collection from my cold, dead hands, and the digitized version from an equally cold, dead hard drive.

All of these are shell scripts or configuration options that work with a standard mpg321 install - none of these change mpg321 itself or expect any non-standard commands. I've mostly tested these in bash and dash, your results may vary in other shells.

## TODOs:
These all need to be implemented and shouldn't be too difficult:
- locate an individual song and play it
- locate songs on a remote mount, copying it locally for speed (and deleting it after playback)
- configure last.fm/audioscrobbler options
- support for non-mp3 file formats (probably with other players, determining which one to use automatically)

This repo is modeled after my alias_lynx project, so these drop right into a .bashrc file, but got their own repository for the sake of convenience and portability. To use, clone the repo and add the following lines to wherever your aliases are stored (most likely .bash_aliases, .bashrc, or .zshrc):

```
if [ -f ~/github/alias_mpg321/mpg321_aliases ]; then
    . ~/github/alias_mpg321/mpg321_aliases
fi
```

Make sure that you use the correct path if you decide to keep your repository somewhere different than I do.

## License and contributions
GPLv3 has been slapped on here. You're welcome to suggest changes 
