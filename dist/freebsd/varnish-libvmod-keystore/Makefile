# $FreeBSD$

PORTNAME=	libvmod-keystore
PORTVERSION=	1.0
CATEGORIES=	www
PKGNAMEPREFIX=	varnish-

MAINTAINER=	e2c2be7ed0f2f336@gmail.com
COMMENT=	Varnish base module (vmod) to interact with key/value store databases

LICENSE=	BSD

# Disable dependency on www/varnish for now as it is still version 3.0.5
#BUILD_DEPENDS=	${LOCALBASE}/include/varnish/varnishapi.h:${PORTSDIR}/www/varnish

USE_GITHUB=	yes
GH_ACCOUNT=	julp
GH_COMMIT=	79fa514
GH_TAGNAME=	${GH_COMMIT}

USES=		cmake:outsource

CMAKE_ARGS=	-DWITH_REDIS:BOOL=OFF -DWITH_MEMCACHED:BOOL=OFF

XFLAGS=		-I${LOCALBASE}/include -I${LOCALBASE}/include/varnish
CFLAGS+=	${XFLAGS}
CPPFLAGS+=	${XFLAGS}

.include <bsd.port.mk>