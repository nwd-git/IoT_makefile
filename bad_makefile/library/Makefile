CC:=gcc
CFLAGS:=-Wall
LIB:=calculator.so
PREFIX?=/usr

.PHONY: all install clean

all: $(LIB)

$(LIB): math_functions.c
	$(CC) $(CFLAGS) -o $@ -c  $^
	
install: $(LIB)
	install -m 644 math_functions.h $(PREFIX)/include

uninstall:

clean:
	rm -f $(LIB)
