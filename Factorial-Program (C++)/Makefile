# Macros
MACROS  = -me
PSROFF  = groff -Tps
DITROFF = groff -Tdvi
CFLAGS  = -O -systype bsd43
LIBS    = "-lncurses -lm -lsdl"
MYFACE  = ":*)"

# target [target...] : [dependent ....]
# 	[ command ...]

# Dependencies
hello: main.o factorial.o hello.o
	$(CC) main.o factorial.o hello.o -o hello

main.o: main.cpp functions.h
	$(CC) -c main.cpp

factorial.o: factorial.cpp functions.h
	$(CC) -c factorial.cpp

hello.o: hello.cpp functions.h
	$(CC) -c hello.cpp

clean:
	-rm *.o *~ core paper

install:
	@echo You must be root to install

# Special Macros
# hello: main.cpp hello.cpp factorial.cpp
# 	$(cc) $(CFLAGS) $? $(LDFLAGS) -o $@

# Alternatively: 

# hello: main.cpp hello.cpp factorial.cpp
# 	$(cc) $(CFLAGS) $@.cpp $(LDFLAGS) -o $@

# More Special Macros
# .cpp.o:
# 	$(cc) $(CFLAGS) -c $<

# Alternatively: 

# .cpp.o: 
# 	$(cc) $(CFLAGS) -c $*.c

