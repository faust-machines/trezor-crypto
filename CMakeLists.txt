if(CONFIG_LIBTREZOR)
zephyr_interface_library_named(LIBTREZOR)

zephyr_include_directories(.)

zephyr_library()
zephyr_library_sources(
    trezor/address.c
    trezor/base32.c
    trezor/base58.c
    trezor/bignum.c
    trezor/bip32.c
    trezor/bip39.c
    trezor/bip39_english.c
    trezor/blake2b.c
    trezor/blake2s.c
    trezor/blake256.c
    trezor/cash_addr.c
    trezor/chacha_drbg.c
    trezor/curves.c
    trezor/ecdsa.c
    trezor/groestl.c
    trezor/hasher.c
    trezor/hmac_drbg.c
    trezor/hmac.c
    trezor/memzero.c
    trezor/nem.c
    trezor/nist256p1.c
    trezor/pbkdf2.c
    trezor/rand.c
    trezor/rc4.c
    trezor/rfc6979.c
    trezor/ripemd160.c
    trezor/script.c
    trezor/secp256k1.c
    trezor/segwit_addr.c
    trezor/sha2.c
    trezor/sha3.c
    trezor/shamir.c
    trezor/slip39.c
)

zephyr_library_link_libraries(LIBTREZOR)
target_link_libraries(LIBTREZOR INTERFACE zephyr_interface)
endif()