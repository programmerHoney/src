# $OpenBSD: Makefile,v 1.24 2020/04/19 16:26:11 schwarze Exp $

REGRESS_TARGETS	 = beforeNAME blank centered nested nf paragraph spacing
REGRESS_TARGETS	+= badargs empty offset-empty offset-neg
REGRESS_TARGETS	+= break broken unclosed

TAG_TARGETS	 = nested paragraph spacing
LINT_TARGETS	 = beforeNAME blank nested badargs break broken unclosed
HTML_TARGETS	 = nested nf paragraph

SKIP_TMAN	 = beforeNAME centered

# groff-1.22.3 defects:
# - a display breaking another block continues indefinitely
# - negative offsets take no effect, but advance the indention on exit

SKIP_GROFF	 = break offset-neg

# adjustment is disabled in groff for now

SKIP_GROFF	+= centered

# groff handles content before NAME differently

SKIP_GROFF	+= beforeNAME

.include <bsd.regress.mk>
