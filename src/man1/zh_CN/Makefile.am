include $(srcdir)/../manpages

mandir = @mandir@/zh_CN

if APPEND_COLOPHON
APPEND_COLOPHON = ${top_srcdir}/utils/append-colophon
else !APPEND_COLOPHON
APPEND_COLOPHON = tee
endif

man_MANS = $(MANPAGES)

%.1: $(srcdir)/../%.1
	$(APPEND_COLOPHON) < $< | opencc -c t2s.json > $@

clean-local:
	rm -f $(man_MANS)
