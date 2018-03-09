# $OpenBSD: Makefile.template,v 1.77 2018/02/09 17:08:33 sthen Exp $

# Only tested on amd64 at the moment
ONLY_FOR_ARCHS =	amd64

COMMENT =	2D image processing library requiring little memory

VERSION =	8.6.3
DISTNAME =	vips-${VERSION}
PKGNAME =	libvips-${VERSION}
SHARED_LIBS =	vips		50.2 \
		vipsCC		50.2 \
		vips-cpp	50.2

CATEGORIES =	graphics

HOMEPAGE =	https://jcupitt.github.io/libvips/

MAINTAINER =	Dave Voutila <dave@sisu.io>

# LGPLv2
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB = 	${COMPILER_LIBCXX} ICE SM X11 Xext Xrender Xt bz2 c
WANTLIB += 	expat ffi fontconfig freetype gio-2.0 glib-2.0 gmodule-2.0
WANTLIB += 	gobject-2.0 gthread-2.0 iconv intl jpeg m pcre pixman-1
WANTLIB	+= 	png tiff xcb xcb-render xcb-shm z

MASTER_SITES =	https://github.com/jcupitt/libvips/releases/download/v8.6.3/

LIB_DEPENDS =		devel/glib2 \
			graphics/tiff \
			graphics/png \
			archivers/bzip2

#SEPARATE_BUILD =	Yes (build in a directory other than WRKSRC)
USE_GMAKE =		Yes
#USE_LIBTOOL=		gnu
CONFIGURE_STYLE =	gnu

.include <bsd.port.mk>
