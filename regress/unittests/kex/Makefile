#	$OpenBSD: Makefile,v 1.19 2025/07/24 06:04:47 djm Exp $

PROG=test_kex
SRCS=tests.c test_kex.c test_proposal.c

# From usr.bin/ssh
SRCS+=sshbuf-getput-basic.c sshbuf-getput-crypto.c sshbuf-misc.c sshbuf.c
SRCS+=sshbuf-io.c atomicio.c sshkey.c authfile.c cipher.c log.c ssh-rsa.c
SRCS+=ssh-ecdsa.c ssh-ed25519.c mac.c umac.c umac128.c hmac.c misc.c
SRCS+=ssherr.c uidswap.c cleanup.c xmalloc.c match.c krl.c fatal.c
SRCS+=addr.c addrmatch.c bitmap.c packet.c dispatch.c canohost.c ssh_api.c
SRCS+=compat.c ed25519.c hash.c
SRCS+=cipher-chachapoly.c chacha.c poly1305.c ssh-ecdsa-sk.c ssh-sk.c
SRCS+=ssh-ed25519-sk.c sk-usbhid.c ssh-pkcs11-client.c

SRCS+=	kex.c
SRCS+=	kex-names.c
SRCS+=	dh.c
SRCS+=	kexdh.c
SRCS+=	kexecdh.c
SRCS+=	kexgex.c
SRCS+=	kexgexc.c
SRCS+=	kexgexs.c
SRCS+=	kexc25519.c
SRCS+=	smult_curve25519_ref.c
SRCS+=	kexgen.c
SRCS+=	kexsntrup761x25519.c
SRCS+=	kexmlkem768x25519.c
SRCS+=	sntrup761.c
SRCS+=	utf8.c

SRCS+=digest-openssl.c
#SRCS+=digest-libc.c

REGRESS_TARGETS=run-regress-${PROG}

run-regress-${PROG}: ${PROG}
	env ${TEST_ENV} ./${PROG} ${UNITTEST_ARGS}

.include <bsd.regress.mk>

LDADD+=-lz
