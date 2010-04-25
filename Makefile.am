sbin_PROGRAMS=trivial.fingerd
trivial_fingerd_SOURCES=fingerd.c
man_MANS=trivial.fingerd.8
EXTRA_DIST=autogen.sh fingerd.plist.in

# launchd config for OS X systems
# http://developer.apple.com/macosx/launchd.html
all: fingerd.plist

fingerd.plist: fingerd.plist.in Makefile
	sed < fingerd.plist.in > fingerd.plist \
		's,_sbindir_,${sbindir},g'

install-data-local:
	@if [ -w /Library/LaunchDaemons ]; then \
	  echo ${INSTALL} -m 644 fingerd.plist /Library/LaunchDaemons/uk.org.greenend.fingerd.plist ;\
	  ${INSTALL} -m 644 fingerd.plist /Library/LaunchDaemons/uk.org.greenend.fingerd.plist ;\
	fi

uninstall-local:
	@if [ -w /Library/LaunchDaemons ]; then \
	  echo launchctl unload /Library/LaunchDaemons/uk.org.greenend.fingerd.plist ;\
	  launchctl unload /Library/LaunchDaemons/uk.org.greenend.fingerd.plist || true ;\
	  echo rm -f /Library/LaunchDaemons/uk.org.greenend.fingerd.plist ;\
	  rm -f /Library/LaunchDaemons/uk.org.greenend.fingerd.plist ;\
	fi
