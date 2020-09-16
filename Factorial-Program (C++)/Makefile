# Macros
MACROS  = -me
PSROFF  = groff -Tps
DITROFF = groff -Tdvi
CFLAGS  = -O -systype bsd43
LIBS    = "-lncurses -lm -lsdl"
MYFACE  = ":*)"

# Dependencies
main.o: main.cpp functions.h
   $(CC) -c main.cpp

factorial.o: factorial.cpp functions.h
   $(CC) -c factorial.cpp

hello.o: hello.cpp functions.h
   $(CC) -c hello.cpp

hello: main.o factorial.o hello.o
   $(CC) main.o factorial.o hello.o -o hello

# Special Macros
hello: main.cpp hello.cpp factorial.cpp
	$(cc) $(CFLAGS) $? $(LDFLAGS) -o $@

Alternatively: 

hello: main.cpp hello.cpp factorial.cpp
	$(cc) $(CFLAGS) $@.cpp $(LDFLAGS) -o $@

# More Special Macros
.cpp.o:
	$(cc) $(CFLAGS) -c $<

Alternatively: 

.cpp.o: 
	$(cc) $(CFLAGS) -c $*.c

