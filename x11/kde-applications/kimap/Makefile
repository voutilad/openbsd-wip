# $OpenBSD$

COMMENT =	job-based API for interacting with IMAP servers
DISTNAME =	kimap-${VERSION}
CATEGORIES =	devel mail

KDE5 =		Yes

SHARED_LIBS +=  KF5IMAP                   0.0 # 5.5

WANTLIB += ${COMPILER_LIBCXX} KF5Codecs KF5ConfigCore KF5CoreAddons
WANTLIB += KF5I18n KF5KIOCore KF5Mime KF5Service Qt5Core m sasl2

MODULES +=	lang/python

BUILD_DEPENDS +=devel/gettext-tools

RUN_DEPENDS =	devel/gettext

LIB_DEPENDS =	devel/kf5/kcoreaddons \
		devel/kf5/kio \
		x11/kde-applications/kmime \
		security/cyrus-sasl2

.include <bsd.port.mk>
