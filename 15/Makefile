all: gradebookadd gradebookdisplay setup

CFLAGS=-g 
LFLAGS=-lssl -lcrypto 

gradebookadd: gradebookadd.o data_skel.o crypto.o
	$(CC) -g -o gradebookadd gradebookadd_skel.o data_skel.o crypto.o $(LFLAGS)

gradebookdisplay: gradebookdisplay_skel.o data_skel.o crypto.o
	$(CC) $(CFLAGS) -o gradebookdisplay gradebookdisplay_skel.o data_skel.o crypto.o $(LFLAGS)

setup: setup.o data_skel.o
	$(CC) $(CFLAGS) -o setup setup_skel.o data_skel.o $(LFLAGS)

gradebookadd.o: gradebookadd_skel.c
	$(CC) $(CFLAGS) -c -o gradebookadd_skel.o gradebookadd_skel.c

gradebookdisplay_skel.o: gradebookdisplay_skel.c
	$(CC) $(CFLAGS) -c -o gradebookdisplay_skel.o gradebookdisplay_skel.c

setup.o: setup_skel.c
	$(CC) $(CFLAGS) -c -o setup_skel.o setup_skel.c

data_skel.o: data_skel.c
	$(CC) $(CFLAGS) -c -o data_skel.o data_skel.c

crypto.o: crypto.c
	$(CC) $(CFLAGS) -c -o crypto.o crypto.c 

clean:
	rm -f *.o
	rm -rf gradebookadd_skel gradebookdisplay_skel setup_skel