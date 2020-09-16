# Macros
MACROS  = -me
PSROFF  = groff -Tps
DITROFF = groff -Tdvi
CFLAGS  = -O -systype bsd43
LIBS    = "-lncurses -lm -lsdl"
MYFACE  = ":*)"

# Special Macros
hello: main.cpp hello.cpp factorial.cpp
	$(cc) $(CFLAGS) $? $(LDFLAGS) -o $@

Alternatively: 

hello: main.cpp hello.cpp factorial.cpp
	$(cc) $(CFLAGS) $@.cpp $(LDFLAGS) -o $@
