project(crontabs_files)

install(FILES periodic.conf DESTINATION libexec/darling/private/etc/defaults)
install(FILES periodic.conf.5 DESTINATION libexec/darling/usr/share/man/man5)

install(FILES
	LaunchDaemons/com.apple.newsyslog.plist
	LaunchDaemons/com.apple.periodic-daily.plist
	LaunchDaemons/com.apple.periodic-monthly.plist
	LaunchDaemons/com.apple.periodic-weekly.plist

	DESTINATION libexec/darling/System/Library/LaunchDaemons)

install(DIRECTORY daily weekly monthly DESTINATION libexec/darling/private/etc/periodic)

install(FILES newsyslog.conf DESTINATION libexec/darling/private/etc)

