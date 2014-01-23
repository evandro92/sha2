---
project: sha2
tagline: SHA-256/-384/-512 hashing
---

## `local sha2 = require'sha2'`

A ffi binding of Aaron Gifford's [SHA-2 implementation][sha2 lib].

----------------------------------- -----------------------------------
`sha2.sha256(s[, size]) -> s`   \   Compute the SHA-2 hash of a string or a cdata buffer.
`sha2.sha256(cdata, size) -> s` \   Return the  binary representation of the hash.
`sha2.sha384(s[, size]) -> s`   \   To get the hex representation, use [glue.tohex].
`sha2.sha384(cdata, size) -> s` \
`sha2.sha512(s[, size]) -> s`   \
`sha2.sha512(cdata, size) -> s`

`sha2.sha256_digest() -> digest` \  Get a SHA-2 digest function that can consume multiple data chunks
`sha2.sha384_digest() -> digest` \  until called with no arguments when it returns the final SHA hash.
`sha2.sha512_digest() -> digest` \
`digest(s[, size])`              \
`digest(cdata, size)`            \
`digest() -> s`

----------------------------------- -----------------------------------

See also: [md5]

[glue.tohex]: glue.html#tohex
[sha2 lib]:   http://www.aarongifford.com/computers/sha.html
