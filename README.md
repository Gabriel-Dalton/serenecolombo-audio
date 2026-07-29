# serenecolombo-audio

The audio archive for serenecolombo.org. The git tree looks empty because it is: all 204 MP3 files are attached to a single release tagged `audio` rather than committed, and 4.4GB of media has no business in git history.

Everything is here: https://github.com/Gabriel-Dalton/serenecolombo-audio/releases/tag/audio

## What is in it

Podcast episodes, chanting and guided meditations, pulled from the WordPress version of the site and deduplicated across its `wp-content/uploads`, `podcast-download` and `podcast-player` paths. The largest group is the `MitM` series at 147 files. The rest are individual chants, suttas and talks.

## How the site uses it

The static build of serenecolombo.org redirects each original WordPress audio URL to the matching release asset through its `vercel.json`, so old links keep working and the site itself ships no audio.

## Adding audio

Upload to the existing `audio` release. Every asset then stays under the same download path and the redirects in the site repo keep resolving. A second release tag would split the archive and mean editing those redirects.
