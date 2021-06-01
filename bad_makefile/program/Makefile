CC:=gcc
Flags:=-Wall -Ipwd
OBJS:=main.o math_functions.o
BIN:=calculator

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(Flags) -o $@ $^ 

clean:
	rm -f $(BIN) $(OBJS)
