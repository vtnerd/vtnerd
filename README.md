## Creator 
### [monero-lws](https://code.leeclagett.com/monero-lws)
  * MyMonero compatible light-wallet server that uses LMDB and ZeroMQ.
  * Useful for non-custodial payment processors (BTCPayserver, etc)
    * webhook/zeromq real-time reporting of incoming funds.
  * Fully non-blocking REST API (`boost::beast`), except for LMDB calls (filesystem based, cannot async).

### [lwsf](https://code.leeclagett.com/lwsf)
  * Client library for LWS protocol
  * [monero_c](https://code.leeclagett.com/monero_c/tree/lwsf) fork for lwsf provides C/Dart API.
    * Only one additional function for C/Dart is needed for fork - all other C/Dart functions are maintained upstream
  * Useful for (light) mobile-wallets, particularly ones based in Flutter

### [lwcli](https://github.com/cifro-codes/lwcli)
  * An experimental TUI (ftxui) Monero wallet with mouse+keyboard support
  * Uses `lwsf` or standard Monero wallet backends (runtime-option)
  * Demonstrates that `lwsf` is viable.

### [Motrix](https://code.leeclagett.com/motrix) 
  * Real-time visualizer for Monero transactions
  * Built with ZeroMQ Pub/Sub, ncurses, and z85 encoding

## Contributor
### [Monero](https://github.com/monero-project/monero/pulls?q=is%3Apr+author%3Avtnerd+)
  * Highlights:
    * Modified Ed25519 library (x86-64 ASM) for direct ECDH needed for Monero wallets
    * Implemented Dandelion++ (p2p protocol) for transaction privacy
    * Added SSL to p2p protocol (still in review, near completion)
    * Updated internal serialization functions to remove intermediate DOM, providing better performance, less memory usage, and better constraints for unpacking (compressed binary protocol to C++). (Not really reviewed - devs are busy :/)

### [boost::spirit](https://github.com/boostorg/spirit/pulls?q=is%3Apr+author%3Avtnerd+)
### [boost::fusion](https://github.com/boostorg/fusion/pulls?q=is%3Apr+author%3Avtnerd+)
