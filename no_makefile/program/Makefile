CC:=gcc
BIN:=calculator
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)
CFLAGS:=-Wall -I$(CURDIR)
PREFIX:=/usr
.PHONY: all install uninstall clean

all: $(BIN) 

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@

$(OBJS): $(SRC)
	$(CC) $(CFLAGS) -c $^

clean: 
	$(RM) $(LIB) $(OBJS) $(BIN)
