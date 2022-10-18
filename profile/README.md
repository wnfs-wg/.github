# Welcome to the WebNative Filesystem (WNFS) Working Group

The Web Native File System (WNFS) is a distributed file system. It is versioned,
logged, programmable, has strong-yet-flexible security, and is fully controlled
by the end user. Service providers can validate writes without reading the
contents of the file system, and minimal metadata is leaked.

WNFS relies heavily on the ”space” side of the space/time trade-off to deliver
performance. As a consequence of this and Merklization, WNFS can provide
advanced functionality such as versioning and delegated or collaborative write
access.

WNFS can be used for offline collaboration, because WNFS forms a state-based
conflict-free replicated data type (CRDT): There exists a commutative and
associative merge function that combines any two (versions of) WNFS roots.

WNFS is content-addressed and thus extremely portable. It may be stored on the
edge, on the end user's device or in the cloud. Devices may also only partially
load a WNFS and still write files and directories.

Please see the [official spec][spec] or [specs](#specs) for more detail.

# Directory

## Suite of Specifications

- [Public WNFS][public-wnfs] (🏁 start here!)
- [Private WNFS][private-wnfs]
- [Namefilters][namefilters]
- [Skip Ratchet][skip-ratchet]

## Libraries

* [Golang][wnfs-go]
* [Rust][wnfs-rust]

## Discussions & Community

- For live chat, join the `#wnfs` channel in the [IPFS discord](https://discord.gg/vj7qWuAyHY)
- For ideas & use cases, feel free to use this repo's [github discussions](https://github.com/wnfs-wg/spec/discussions/2)

## External Resources

Note that while the below all describe WNFS at the time they were written, the
spec has undergone updates. Please refer to the [latest spec][spec] if you
have questions.

### Presentations

- [A Distributed File System for Secure P2P Applications](https://www.youtube.com/watch?v=-f4cH_HQU4U) by Brooklyn Zelenka (Strange Loop 2022)
- [WebNative File System](https://www.youtube.com/watch?v=3se17NAS-Lw) by Brooklyn Zelenka (IPFS bing 2022)
- [Shared Private Files Design in Webnative's WNFS](https://vimeo.com/534517727) by Brooklyn Zelenka

### Related Skip-Ratchet Implementations

- [Go][skip-go]
- [Rust][skip-rust]
- [Typescript][skip-ts]

### Related Papers

- [Skip Ratchet: A Hierarchical Hash System][paper] by Brooklyn Zelenka


[wnfs-go]: https://github.com/wnfs-wg/wnfs-go
[paper]: https://eprint.iacr.org/2022/1078.pdf
[public-wnfs]: https://github.com/wnfs-wg/spec/blob/main/spec/public-wnfs.md
[private-wnfs]: https://github.com/wnfs-wg/spec/blob/main/spec/private-wnfs.md
[namefilters]: https://github.com/wnfs-wg/spec/blob/main/spec/namefilter.md
[skip-ratchet]: https://github.com/wnfs-wg/spec/blob/main/spec/skip-ratchet.md
[spec]: https://github.com/wnfs-wg/spec
[skip-go]: https://github.com/wnfs-wg/wnfs-go
[skip-rust]: https://github.com/wnfs-wg/rs-skip-ratchet
[skip-ts]: https://github.com/fission-suite/webnative/blob/matheus23/wnfs2/src/fs/data/private/spiralratchet.ts
[wnfs-rust]: https://github.com/wnfs-wg/rs-wnfs
[wnfs-ts]: https://github.com/fission-codes/webnative/blob/main/README.md#web-native-file-system
