#
# makefile for TINY
# Borland C Version
# K. Louden 2/3/98
#
# modified at Oct. 29, 2022 in SJTU
#

CC = gcc

CFLAGS =

oS = main.o util.o lexer.o

main.o: ../main.c ../globals.h ../util.h ../lexer.h
	$(CC) $(CFLAGS) -c ../main.c

lexer.o: ../lexer.c ../lexer.h ../util.h ../globals.h
	$(CC) $(CFLAGS) -c ../lexer.c

util.o: ../util.c ../util.h ../globals.h
	$(CC) $(CFLAGS) -c ../util.c

clean:
	del main.o
	del util.o
	del lexer.o

rmexe:
	-rm bin/lexer
	-rm bin/parser

lexer: $(oS)
	$(CC) $(CFLAGS) -o bin/lexer $(oS)

testl:
	-bin/lexer test/sample.tny
