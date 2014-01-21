debug: generate-debug install-debug clear-log
	ant installd
	adb logcat -c
	adb logcat ELC:I *:S

clean:
	rm -r bin/* && rm -r gen/*

generate-debug:
	ant debug
	
generate-release:
	ant release	

install-debug:
	ant installd

clear-log: 
	adb logcat -c

debug-all: generate-debug install-debug clear-log
	adb logcat *:E

convert-from-eclipse:
	android update project -p . --target 8