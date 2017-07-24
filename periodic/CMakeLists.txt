project(crontabs_periodic)

add_darling_executable(periodic-wrapper periodic-wrapper.c)

install(TARGETS periodic-wrapper DESTINATION libexec/darling/usr/libexec)
install(FILES periodic-wrapper.8 periodic.8 DESTINATION libexec/darling/usr/share/man/man8)
install(FILES periodic.sh DESTINATION libexec/darling/usr/sbin RENAME periodic)

