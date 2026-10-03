# video-door

One small page with a web address, so that an HTML file opened from disk can still play a
YouTube video. YouTube refuses to play inside any page that cannot say what address it came
from (its "Error 153", enforced since 2025), and a double-clicked file has no address. This
page has one. A file frames it with `?v=<video id>` and drives the player through
`postMessage`; the file itself never needs hosting.

Generic by design: it knows nothing about any file that uses it, and it is the same page
for all of them. `index.html` is the whole thing; the protocol is described at the top of it.
