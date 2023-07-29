# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: filipe <filipe@student.42.fr>              +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/05/05 15:27:36 by fmilheir          #+#    #+#              #
#    Updated: 2023/07/29 17:32:55 by filipe           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC = cc
CFLAGS = -Wall -Wextra -Werror #-fsanitize=thread
NAME = philo
HEADER = philo.h
SRC = philo.c utils.c parsing.c routine.c initialisation.c create.c \
		check_death.c
OBJ_SRC = $(SRC:.c=.o)

all : $(NAME)

$(NAME) : $(OBJ_SRC) $(HEADER)
	$(CC) $(CFLAGS) $(OBJ_SRC) -o $(NAME)

%.o  : %.c $(HEADER)
	$(CC) $(CFLAGS) -c $<

clean :
	$(RM) $(OBJ_SRC)

fclean : clean
	$(RM) $(NAME)

re : fclean all

r:
	make re && clear && ./philo 200 800 200 200

.PHONY: all fclean clean re 