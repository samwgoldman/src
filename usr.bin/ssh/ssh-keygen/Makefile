#	$OpenBSD: Makefile,v 1.37 2019/12/13 19:11:14 djm Exp $

.PATH:		${.CURDIR}/..

SRCS=	ssh-keygen.c ${SRCS_MODULI}
SRCS+=	atomicio.c authfd.c cleanup.c dns.c fatal.c hmac.c hostfile.c \
	readpass.c utf8.c sshsig.c
SRCS+=	${SRCS_BASE} ${SRCS_KEY} ${SRCS_KEYP} ${SRCS_KRL} ${SRCS_UTL} \
	${SRCS_PKCS11} ${SRCS_SK_CLIENT}

PROG=	ssh-keygen

BINDIR=	/usr/bin

.include <bsd.prog.mk>

LDADD+=	-lcrypto -lutil
DPADD+=	${LIBCRYPTO} ${LIBUTIL}
