project(trezor)
cmake_minimum_required(VERSION 3.20)

add_library(trezor)
target_compile_options(trezor PRIVATE -Wall -Wextra)
set_target_properties(trezor PROPERTIES C_STANDARD 11)

target_include_directories(trezor PUBLIC crypto)

target_sources(trezor PRIVATE
    crypto/address.c
    crypto/base32.c
    crypto/base58.c
    crypto/bignum.c
    crypto/bip32.c
    crypto/bip39.c
    crypto/bip39_english.c
    crypto/blake2b.c
    crypto/blake2s.c
    crypto/blake256.c
    crypto/cash_addr.c
    crypto/chacha_drbg.c
    crypto/curves.c
    crypto/ecdsa.c
    crypto/groestl.c
    crypto/hasher.c
    crypto/hmac_drbg.c
    crypto/hmac.c
    crypto/memzero.c
    crypto/nem.c
    crypto/nist256p1.c
    crypto/pbkdf2.c
    crypto/rand.c
    crypto/rc4.c
    crypto/rfc6979.c
    crypto/ripemd160.c
    crypto/script.c
    crypto/secp256k1.c
    crypto/segwit_addr.c
    crypto/sha2.c
    crypto/sha3.c
    crypto/shamir.c
    crypto/slip39.c
)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")