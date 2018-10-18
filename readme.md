# ed25519

## why this repo

This repo is copy from golang.org/x/crypto/ed25519.

Because of golang.org/x/crypto/ed25519 did not expose some useful API, so I fork it and create this repo.

# API

The API is same with golang.org/x/crypto/ed25519, but it offers some addition API as following

import "github.com/bitnexty/ed25519/edwards25519"

## edwards25519.ScReduce

## edwards25519.ScMinimal

## edwards25519.GeScalarMultBase

## example

For example, we can use this repo to convert Monero secret key to public key:

```
import "github.com/bitnexty/ed25519/edwards25519"

// MoneroKey monero key 32 bytes
type MoneroKey [32]byte

// SecretToPubkey derive secret key to public key
// secret key is NOT ed25519 private key
func SecretToPubkey(secret []byte) MoneroKey {
	if len(secret) != XMRKeyLen {
		log.Fatal("SecretToPubkey: secret length should be 32")
	}

	var (
		A edwards25519.ExtendedGroupElement
		hBytes [XMRKeyLen]byte
		publicKeyBytes [XMRKeyLen]byte
		pkBytes MoneroKey
	)

	copy(hBytes[:], secret[:])
	edwards25519.GeScalarMultBase(&A, &hBytes)
	A.ToBytes(&publicKeyBytes)

	copy(pkBytes[:], publicKeyBytes[:])
	return pkBytes
}
```
