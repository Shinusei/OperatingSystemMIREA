all: elf.c new_elf.c main.c upx_start.asm upx_end.asm new_main.c
		nasm -f elf64 upx_start.asm
		nasm -f elf64 upx_end.asm
		gcc -o main.exe upx_start.o main.c upx_end.o
		gcc -o elf.exe elf.c
		gcc -o new_elf.exe new_elf.c
		gcc -o new_main.exe upx_start.o new_main.c upx_end.o
clean:
		rm -f *.exe *.o
