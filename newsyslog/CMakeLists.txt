project(crontabs_newsyslog)

add_darling_executable(newsyslog newsyslog.c ptimes.c)

install(TARGETS newsyslog DESTINATION libexec/darling/usr/sbin)
install(FILES newsyslog.8 DESTINATION libexec/darling/usr/share/man/man8)
install(FILES newsyslog.conf.5 DESTINATION libexec/darling/usr/share/man/man5)


