gcc=CC
main.v1:main.c lib/libcal.a
	$(CC) -o $@ $< -l cal -L lib -I ./include
lib/libcal.a:lib/add.o lib/sub.o
	ar rcs lib/libcal.a
lib/add.o:src/add.c include/add.h
	$(CC) -c $< -o lib/add.o -I ./include
lib/sub.o:src/sub.c include/sub.h
	$(CC) -c $< -o lib/sub.o -I ./include
.PHONY: clean
	rm -f lib/*o
	rm -f main
