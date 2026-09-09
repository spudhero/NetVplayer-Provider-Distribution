# NetVplayer Provider Distribution

Signed Provider packages and download indexes for the source-free NetVplayer macOS shell.

- `stable/index.json`: official distribution index. It currently contains no Providers or video sources.
- `diagnostics/index.json`: a separate opt-in channel for offline transport diagnostics. Diagnostic packages contain no video sources or playback URLs and are never selected by the shell's stable index.
- `public-keys.json`: pinned public verification keys. Private signing keys and Provider implementation repositories are not stored here.

Release assets are built in the private Provider repository. Every package and index is Ed25519-signed; packages use the `community-adhoc` macOS signing profile. Downloading a package does not imply Apple notarization.

The application starts without video sources. Users configure their own content separately. This distribution repository is maintained by [spudhero](https://github.com/spudhero).
