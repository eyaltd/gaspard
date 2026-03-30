##
## EPITECH PROJECT, 2025
## Makefile
## File description:
## Makefile
##

BINARY_NAME = test

CC = epiclang

SRC = src/add.c \
      tests/tests_main.c \

OBJ = $(SRC:.c=.o)

HEADERS = -I./include/

LIBRARIES = -lcriterion

all: $(OBJ)
    $(CC) -o ${BINARY_NAME} $(OBJ) $(HEADERS) $(LIBRARIES)

%.o: %.c
    $(CC) -c $< -o $@ $(HEADERS)

tests_run:

clean:
    rm -f ${OBJ}

fclean: clean
    rm -f ${BINARY_NAME}

re: fclean all

valgrind:
    valgrind --log-file="log-valgrind.txt" --track-origins=yes --show-reachable=yes --leak-check=full --leak-resolution=high ./$(BINARY_NAME)

.PHONY: clean fclean re valgrind
