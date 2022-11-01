# release-archive-with-hash
Uploads a source archive and hash at every release.

GitHub source archives are generated on demand and not guaranteed to have a constant hash. This is a problem when you try to verify that old releases have not changed. This tool uploads a release artifact that will have the same hash in perpetuity and a text file containing the hash.
