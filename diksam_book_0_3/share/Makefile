TARGET = share.o
CC=gcc
CFLAGS = -c -g -I../include -DDEBUG -DDKM_WINDOWS -Wall -ansi -pedantic -Wswitch-enum
OBJS = dispose.o \
  opcode.o \
  disassemble.o \
  wchar.o \
  util.o

$(TARGET):$(OBJS)
	ld -r -o $@ $(OBJS)
.c.o:
	$(CC) $(CFLAGS) -I../include $*.c
disassemble.o: disassemble.c ../include/DBG.h ../include/share.h \
  ../include/DVM_code.h ../include/DVM.h
dispose.o: dispose.c ../include/MEM.h ../include/DBG.h \
  ../include/DVM_code.h ../include/DVM.h
opcode.o: opcode.c ../include/share.h ../include/DVM_code.h \
  ../include/DVM.h
util.o: util.c ../include/DBG.h ../include/MEM.h ../include/share.h \
  ../include/DVM_code.h ../include/DVM.h
wchar.o: wchar.c ../include/DBG.h ../include/MEM.h ../include/DVM.h
