# Makefile

LIBRARIES = WiFiNINA IRremote ArduinoJson ArduinoHttpClient Arduino_LSM6DS3 DS3231
BOARD = arduino:avr:mega
PORT = /dev/$$(ls -al /dev/ | grep cu.usbmodem | awk '{ print $$9 }')

# .PHONY: all

# all: install compile upload monitor

# init: install
# 	brew bundle
# 	arduino-cli core install arduino:samd

# install:
# 	arduino-cli lib install $(LIBRARIES)

compile:
		arduino-cli compile --fqbn $(BOARD)

upload:
		arduino-cli upload -p $(PORT) --fqbn $(BOARD) $(SKETCH) && sleep 4;

monitor:
		arduino-cli monitor -p $(PORT)
