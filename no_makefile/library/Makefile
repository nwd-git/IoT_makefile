CC:=gcc
LIB:=libfilereader.so
BIN:=main
PROGRAM_SRC:=main.c
OBJS:=$(PROGRAM_SRC:.c=.o)
LIB_SRC:=file_reader.c
LDFLAGS:=-L$(CURDIR) -lfilereader
CFLAGS:=-Wall -I$(CURDIR)
PREFIX?=/usr
.PHONY: all install uninstall clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@ $(LDFLAGS) 

$(OBJS): $(PROGRAM_SRC)
	$(CC) $(CFLAGS) -c $^
	
$(LIB): $(LIB_SRC)
	$(CC) $(CFLAGS) -fpic -shared -o $@ -c $^

install: $(LIB)
	install -m 644 $(LIB) $(PREFIX)/lib
	install -m 644 file_reader.h $(PREFIX)/include
uninstall:
	$(RM) $(PREFIX)/include/file_reader.h
	$(RM) $(PREFIX)/lib/$(LIB)
clean:
	$(RM) $(BIN) $(OBJS) $(LIB)
