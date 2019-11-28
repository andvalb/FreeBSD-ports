# $FreeBSD$

PORTNAME=	libreSense-upgrade
PORTVERSION=	0.69
CATEGORIES=	sysutils
MASTER_SITES=	# empty
DISTFILES=	# empty
EXTRACT_ONLY=	# empty

MAINTAINER=	coreteam@pfsense.org
COMMENT=	libreSense upgrade script

LICENSE=	APACHE20

NO_MTREE=	yes
NO_BUILD=	yes

PLIST_FILES=	libexec/libreSense-upgrade \
		sbin/libreSense-upgrade

do-extract:
	@${MKDIR} ${WRKSRC}
	${CP} -r ${FILESDIR}/* ${WRKSRC}

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/sbin
	${MKDIR} ${STAGEDIR}${PREFIX}/libexec
	${INSTALL_SCRIPT} ${WRKSRC}/libreSense-upgrade \
		${STAGEDIR}${PREFIX}/libexec
	${INSTALL_SCRIPT} ${WRKSRC}/libreSense-upgrade.wrapper \
		${STAGEDIR}${PREFIX}/sbin/libreSense-upgrade

.include <bsd.port.mk>
