SUBDIRS = macros2 doc-build

EXTRA_DIST = \
	autogen.sh \
	gnome-common.doap \
	doc/usage.txt \
	ChangeLog.pre-git

DISTCHECK_CONFIGURE_FLAGS = --disable-silent-rules

# Build ChangeLog from GIT  history
ChangeLog:
	$(AM_V_GEN) if test -d $(top_srcdir)/.git; then \
		GIT_DIR="$(top_srcdir)/.git" git log --stat > $@; \
	fi

dist: ChangeLog

.PHONY: ChangeLog
