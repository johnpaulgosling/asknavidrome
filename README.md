# AskNavidrome

[![Docker Container](https://github.com/johnpaulgosling/asknavidrome/actions/workflows/build_image.yml/badge.svg)](https://github.com/johnpaulgosling/asknavidrome/actions/workflows/build_image.yml)

This fork of [rosskouk's AskNavidrome v1.2.2](https://github.com/rosskouk/asknavidrome/releases/tag/v1.2.2) adds two new features and one bug fix:

- **Shuffle a playlist by name** — Search your Navidrome playlists by name and play them in a randomised order. Example phrases:
  - "Shuffle the *playlist* playlist"
  - "Shuffle and play the *playlist* playlist"
  - "Play the *playlist* playlist on shuffle"
  - "Play *playlist* playlist shuffled"
  - "Start the *playlist* playlist on shuffle"
  - "Put on the *playlist* playlist in shuffle mode"
  - "Play a shuffled *playlist* playlist"
- **Play a song by title** — Search your library by song title and immediately start playing the first matching result. Example phrases:
  - "Play the song *title*"
  - "Play *title*"
- **Bug fix: single song no longer repeats** — When playing a single song, Alexa would incorrectly re-queue and repeat it indefinitely. The `PlaybackNearlyFinished` handler now correctly detects an empty queue and stops playback.

**AskNavidrome** is an Alexa skill which allows you to play music hosted on a SubSonic API compatible media server, like Navidrome.

You can stream your own music collection to your Echo devices without the restrictions you would normally face with regular 
streaming services like Amazon Music or Spotify.  AskNavidrome allows you to:

- Skip backwards and forwards in your current queue or playlist without limitation.
- Avoid paying subscription costs.
- Avoid being forced to listen to adverts at regular intervals.
- Actually use the music collection you have already paid for!
- Run the service on a PC directly or inside a Docker container.

See the full documentation [here](https://rosskouk.github.io/asknavidrome). Note that the documentation is hosted on rosskouk's GitHub site and installation is identical, **except** the Docker Compose file should use this repo's image:

```yaml
image: 'ghcr.io/johnpaulgosling/asknavidrome:latest'
```
