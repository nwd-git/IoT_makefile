CC:=gcc
LIB:=file_reader.so
BIN:=main
SRC:=$(wildcard *.c)
OBJS=$(SRC:.c=.o)
CFLAGS:=-Wall -Ipwd
PREFIX?=/usr
.PHONY: all install uninstall clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@ 

$(OBJS): $(SRC)
	$(CC) $(CFLAGS) -c $^
	
$(LIB): file_reader.c
	$(CC) $(CFLAGS) -o $@ -c $^

install: $(LIB)
	install -m 644 file_reader.h $(PREFIX)/include
uninstall:
	rm -f $(PREFIX)/include/file_reader.h

clean:
	rm -f $(BIN) $(OBJS) $(LIB)
