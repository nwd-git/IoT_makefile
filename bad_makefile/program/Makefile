CC:=gcc
CFLAGS:=-Wall -I$(CURDIR)
OBJS:=main.o math_functions.o
BIN:=calculator
.PHONY: all clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(Flags) -o $@ $^ 

clean:
	$(RM) $(BIN) $(OBJS)
