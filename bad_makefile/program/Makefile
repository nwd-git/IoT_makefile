CC=gcc
CFLAGS:=-Wall -I$(CURDIR)
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)
BIN:=calculator
.PHONY: all clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) $^ -o $@ 
$(OBJS): $(SRC)
	$(CC) $(CFLAGS) -c $^
clean:
	$(RM) $(BIN) $(OBJS)
