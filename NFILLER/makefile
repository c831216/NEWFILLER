CC = gcc
NAME = cman.filler
FLAGS = -Wall -Werror -Wextra
SRC = ./main.c\

LIBFT = ./libft
OBJ = $(SRCS:.c=.o)

all: NAME

NAME:
	@ make -C ./libft
	@ $(CC) -o $(NAME) $(FLAGS) $(SRC) -L $(LIBFT) -lft
	@ echo "CMAN is ready for battle!"

clean:
	@ make -C ./libft/ clean
	@ echo "Objects Removed!"

fclean: clean
	@ make -C ./libft/ fclean
	@ rm -f *.filler
	@ rm -f *.a
	@ echo "Removed All!"

re: fclean all

norm:
	@ norminette ./Includes/*.h
	@ norminette ./srcs/*.c
	@ norminette ./libft/*.c
	@ norminette ./libft/*.h

.PHONY: all clean fclean re norm
