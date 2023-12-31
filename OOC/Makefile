#============================================================================
# Object Oriented C, an object-oriented programming facility for C.
# Copyright (C) by Zack T Smith. (original author)
# Copyright (C) 2023 by Kristian Kadlubiak.
# This is covered by the Lesser GNU Public License version 3.
#============================================================================

CFLAGS= -g -Wno-conditional-type-mismatch -Wl,-z,noexecstack
CC=gcc -Wall
SRC=main.c 
OBJ=main.o
LIB= 
OOC_SRC= ObjectOriented.c Object.c Image.c MutableImage.c Double.c Int.c Array.c MutableArray.c SimpleGraphing.c String.c MutableString.c Font.c FontBuiltin.c Console.c DateTime.c FontPK.c cmr5.c cmr6.c cmr9.c cmr12.c Log.c
OOC_OBJ= ObjectOriented.o Object.o Image.o MutableImage.o Double.o Int.o Array.o MutableArray.o SimpleGraphing.o String.o MutableString.o Font.o FontBuiltin.o Console.o DateTime.o FontPK.o cmr5.o cmr6.o cmr9.o cmr12.o Log.o

# Note: Mac 32-bit linking no longer supported on Mac OS as of 10.14.

OOC64.a: ${OOC_SRC}
	${CC} ${CFLAGS} -c ${OOC_SRC}
	ar rvs OOC64.a ${OOC_OBJ}

OOC32.a: ${OOC_SRC}
	${CC} -m32 ${CFLAGS} -c ${OOC_SRC}
	ar rvs OOC32.a ${OOC_OBJ}

ARMOOC32: ${OOC_SRC}
	${CC} ${CFLAGS} -c ${OOC_SRC}
	ar rvs OOC32.a ${OOC_OBJ}

ARMOOC64: ${OOC_SRC}
	${CC} ${CFLAGS} -c ${OOC_SRC}
	ar rvs OOC64.a ${OOC_OBJ}

clean:
	chmod 644 *.c *.h *.txt Makefile*
	rm -f ${OOC_OBJ} OOC32.a OOC64.a

