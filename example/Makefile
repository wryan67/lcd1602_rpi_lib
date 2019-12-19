# Build lcd1602 test program

CC       := cc
CFLAGS   := -c -O2 -Wall 
LDFLAGS  := -lwiringPi -lwiringPiDev -lwiringPiLCD101rpi
SOURCES  := lcd1602.c

OBJECTS=$(SOURCES:%.c=../obj/%.o)
HEADERS=$(SOURCES:%.c=%.h)
EXECUTABLE=lcd1602

all:   $(SOURCES) $(EXECUTABLE)
tasks: all

$(EXECUTABLE): $(OBJECTS) 
	@echo Compiling $@
	@mkdir -p ../bin
	@$(CC) $(OBJECTS) $(LDFLAGS) -o $@


../obj/%.o: %.h %.c
	@echo compiling $(*D)/$(*F).c
	@mkdir -p ../obj
	@$(CC) $(CFLAGS) $(*D)/$(*F).c -o $@


clean:
	@rm -rf ../obj/ $(EXECUTABLE)

