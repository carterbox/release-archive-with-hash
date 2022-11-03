# release-archive-with-hash
Upload a source archive and hash at every tagged release.

GitHub source archives are generated on demand and not guaranteed to have a
constant hash. This is a problem when you try to verify that old releases have
not changed. This tool uploads a release archive (that will have the same hash
in perpetuity regardless of GitHubs archive cache invalidation) and a text file
containing the hash of the archive.


```yaml
name: Upload a source archive and hash at every tagged release

on:
  push:
    tags:
    # Use pattern matching to only run on version release tags
      - "v*.*.*"

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: carterbox/release-archive-with-hash@main
```
