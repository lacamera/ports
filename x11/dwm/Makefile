V= 6.3
DISTNAME= dwm-${V}
CATEGORIES=	x11
COMMENT= dynamic window manager
HOMEPAGE= https://dwm.suckless.org/
MAINTAINER=	Francesco La Camera <fm@lacamera.org>
PERMIT_PACKAGE=	Yes
WANTLIB= X11 Xinerama Xft c fontconfig
MASTER_SITES= https://dl.suckless.org/dwm/
RUN_DEPENDS= 
MAKE_ENV= LDFLAGS="${LDFLAGS}" \
			X11INC=${X11BASE}/include \
			X11LIB=${X11BASE}/lib
NO_TEST= Yes
do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/dwm ${PREFIX}/bin/
	${INSTALL_MAN} ${WRKSRC}/dwm.1 ${PREFIX}/man/man1/
	sed -i s/VERSION/${V}/g ${PREFIX}/man/man1/dwm.1
.include <bsd.port.mk>
