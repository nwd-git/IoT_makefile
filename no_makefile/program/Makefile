CC:=gcc
LIB_H:=$(wildcard *.h)
LIB:=$(LIB_H:.h=.so)
BIN:=calculator
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)
CFLAGS:=-Wall -Ipwd
PREFIX:=/usr
.PHONY: all install uninstall clean

all: $(BIN) 

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

$(OBJS): $(SRC)
	$(CC) $(CFLAGS) -c $^

$(LIB): maths.c 
	$(CC) $(CFLAGS) -o $@ -c $<

install: $(LIB)
	install -m 644 usage.h $(PREFIX)/include
	install -m 644 maths.h $(PREFIX)/include
uninstall:
	rm -f $(PREFIX)/include/usage.h
	rm -f $(PREFIX)/include/maths.h

clean: 
	rm -f $(LIB) $(OBJS)
