ASM = nasm
AMFLAGS = -f elf64
LD = ld
LDFLAGS =
SRCS = $(wildcard *.asm)
OBJS = $(SRCS:.asm=.o)
TARGET = p-h

all: $(TARGET)

$(TARGET): $(OBJS)
	$(LD) $(LDFLAGS) -o $@ $^

%.o: %.asm
	$(ASM) $(AMFLAGS) $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)

