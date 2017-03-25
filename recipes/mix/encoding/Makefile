LANGUAGE = zh_CN
ENCODE_TO = utf-8
DIRTXT = $(shell ls | grep -v -e 'Makefile' -e 'sources' -e 'targets' -e 'provide')
DIROUT = $(DIRTXT:=.o)

all: $(DIROUT)

%.o: %
		enca -L $(LANGUAGE) -x $(ENCODE_TO) $^
		echo "" >> provide

install-tools:
	echo "No tools required"

.PHONY: all install-tools
