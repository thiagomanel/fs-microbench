CC=gcc
CCFLAGS += -g -Wall -Wextra

# created to the list
MAIN = rr rw seqr seqw background
all : $(MAIN)

rr.o : rr.c
	$(CC) $(CCFLAGS) -c rr.c

rr : rr.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt

rw.o : rw.c
	$(CC) $(CCFLAGS) -c rw.c

rw : rw.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt

seqr.o : seqr.c
	$(CC) $(CCFLAGS) -c seqr.c

seqr : seqr.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt -lm

seqw.o : seqw.c
	$(CC) $(CCFLAGS) -c seqw.c

seqw : seqw.o
	$(CC) $(CCFLAGS) $^ -o $@ -pthread -lrt -lm

background.o : background.c
	$(CC) $(CCFLAGS) -c background.c

background : background.o
	$(CC) $(CCFLAGS) $^ -o $@

clean :
	rm -rf $(MAIN) *.o
