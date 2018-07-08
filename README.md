# GNL(42_project)
The aim of this project is make a function that returns a line ending with a newline, read from a file descriptor.

The user must create simple main.c and call 'get_next_line':
```
#include "libft/libft.h" //my own library
#include "fcntl.h" //function 'open'
#include "get_next_line.h"

int main()
{
  char *line;
  int fd = open("main.c", O_RDONLY);
  get_next_line(fd, &line);
  ft_putstr(line);
  return (0);
}
```
# Compiling
```
make -C libft/
gcc -Wall -Wextra -Werror get_next_line.c main.c -L libft/ -lft
```
