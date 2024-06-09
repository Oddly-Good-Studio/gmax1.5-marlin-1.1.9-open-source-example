# Makefile

LIBRARIES = U8glib
BOARD = arduino:avr:mega
PORT := $(shell arduino-cli board list | grep $(BOARD) | awk '{ print $$1 }')

.PHONY: all

all: install compile upload monitor

# init: install
	# arduino-cli core install arduino:avr:mega

install:
	arduino-cli lib install $(LIBRARIES)

compile:
		arduino-cli compile --fqbn $(BOARD)

upload:
		arduino-cli upload -p $(PORT) --fqbn $(BOARD) $(SKETCH) && sleep 4;

monitor:
		arduino-cli monitor -p $(PORT)
