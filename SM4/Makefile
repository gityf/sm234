CC=gcc -g  $(CFLAGS) -DLINUX -w
SHARED_FLAG = -fPIC -shared

PROJECT = sm4test

INC  = -I./
OBJ = sm4.o sm4test.o

MODULE =  -lcrypto

all : ${OBJ} $(PROJECT)

$(PROJECT) :
	$(CC) ${OBJ} -o $(PROJECT) $(INC) $(MODULE)

clean:
	rm -rf *.o *.a *.so

%.o : %.cpp
	$(CC) $(SHARED_FLAG) -c $< $(INC)
%.o : %.c
	$(CC) $(SHARED_FLAG) -c $< $(INC)
