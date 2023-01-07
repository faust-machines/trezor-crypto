target_sources(trezor-crypto PRIVATE
    address.c
    base32.c
    base58.c
    bignum.c
    bip32.c
    bip39_english.c
    blake2b.c
    blake2s.c
    blake256.c
    cash_addr.c
    chacha_drbg.c
    curves.c
    ecdsa.c
    groestl.c
    hasher.c
    hmac_drbg.c
    memzero.c
    nist256p1.c
    pbkdf2.c
    rand.c
    rc4.c
    rfc6979.c
    ripemd160.c
    script.c
    secp256k1.c
    segwit_addr.c
    sha2.c
    sha3.c
    shamir.c
    slip39.c
    # zkp_bip340.c
    # zkp_context.c
    # zkp_ecdsa.c
)