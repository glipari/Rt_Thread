CC = gcc
JDK_PATH=/usr/lib/jvm/java-8-openjdk-amd64

CFLAGS = -Wall -fPIC -I$(JDK_PATH)/include -I$(JDK_PATH)/include/linux
LDFLAGS = -lpthread

all : libJNITest.so

libJNITest.so : RtThread.o 
	$(CC) $(LDFLAGS) $^ -shared -o $@ 

%.o : %.c
	$(CC) -c $(CFLAGS) $< -o $@ 

clean :
	rm -rf libJNITest.so
	rm -rf *.o 



