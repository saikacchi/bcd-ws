# BTS YouTube Music Scrobble Fix

Web Scrobbler edits that make BTS and member solo tracks played on **YouTube Music** scrobble with the same metadata as Spotify, so they're recognized correctly by b-cd.app and other scrobble trackers.

YouTube Music often reports titles, album names and artists differently from Spotify: Korean titles instead of English ones, different punctuation and spacing, different version labels. Trackers that match against Spotify's catalog don't recognize those plays, this file corrects them in Web Scrobbler.

## What's included

- **[`bts-ytmusic-edits.json`](bts-ytmusic-edits.json)**: the Web Scrobbler edits file. Needs to be added to each instance of WebScrobbler (if you use multiple profiles!)
- **[`playlist_links.md`](playlist_links.md)**: one YouTube Music playlist per album, containing the album audio tracks in order. Used to grab the actual album track (free youtube music does weird things to album tracks)

## Setup

1. **Back up your current edits.** In Web Scrobbler's options, go to the edited tracks section and export them first. If you've made no edits, make one to initiate the process (start any song, open the WebScrobbler extension on the tab playing music, click the pencil, then save - delete this before importing!)
2. **Import `bts-ytmusic-edits.json`** from the same section.
3. **Reload any open YouTube Music tabs.** Web Scrobbler reads edits when a track starts, so a tab that was already open keeps the old metadata until it's reloaded.

To check that it's working, play a track from *MAP OF THE SOUL : 7 ~ THE JOURNEY ~* and look at the Web Scrobbler popup. With the edits applied, the album name has a space before the colon (`MAP OF THE SOUL : 7`). Without them, it doesn't. (`MAP OF THE SOUL: 7`)

## If using a free YT Music account, grab the 'premium' track from the playlists, not the album pages

On free or logged-out YouTube Music accounts, playing an album page often substitutes music videos, live versions or the wrong-language version for some tracks. For example, the Korean IDOL music video plays in place of IDOL (Japanese ver.) on MOTS: 7 Journey.

The playlists in [`playlist_links.md`](playlist_links.md) were built from the album audio tracks and play the correct versions on **any** account, free or Premium. Adding tracks from these playlists to your own playlists keeps the correct versions too. Adding them from an album page may not.

## Troubleshooting

**Nothing changed after importing.** Reload the YouTube Music tab.

**A track still scrobbles wrong.** Check whether it's playing a music video (the player shows video instead of album art). Use the matching playlist instead of the album page. If it's an album track from the playlist and still wrong, please report it with the track name and the `v=` ID from the URL.

**A release isn't covered.** Tracks that only appear on another artist's release (features and collaborations) aren't included.

**Whatever else**: dm @saika (on bcd) or @ksaikacchi on twt!

