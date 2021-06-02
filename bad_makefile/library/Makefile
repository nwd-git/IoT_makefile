CC:=gcc
CFLAGS:=-Wall 
CPPFLAGS:= -fpic -shared
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)
LIB:= libcalculator.so
PREFIX?=/usr

.PHONY: all install uninstall clean

all: $(LIB)

$(LIB): $(SRC) 
	$(CC) $(CFLAGS) $(CPPFLAGS) -o $@ -c  $^
	
install: $(LIB)
	install -m 644 math_functions.h $(PREFIX)/include
	install -m 644 $(LIB) $(PREFIX)/lib/$(LIB)

uninstall:
	$(RM) $(PREFIX)/include/math_functions,h
	$(RM) $(PREFIX)/lib/$(LIB)
clean:
	$(RM) $(LIB) $(BIN) $(OBJS)
