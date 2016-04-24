# Root Key

Your root key is a key pair like all your sub-keys. The difference between a sub-key and your root key, is that your root key is almost never used, and only allowed to certify other keys. It cannot be used for `encryption`, `signing` or `authentication`, we use sub-keys for those.

Your root key is stored in cold storage, and only ever used on a computer that cannot physically interact with any other device (airgapped) and that doesn't remember anything after shutdown (most likely Tails).

Your root key is used once a year to generate new sub-keys. It may also be used to sign other peoples keys for the [Web of Trust](https://en.wikipedia.org/wiki/Web_of_trust).

## OPSEC

The physical and operation security of your root key is the most important of all. If anything nefarious happens to your root key, or if you lose control of it, your sub-keys can no longer be trusted and should not be used. If this happens, your root key needs to be revoked, a new root key and sub-keys will then need to be created.