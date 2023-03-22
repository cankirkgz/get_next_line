# get_next_line

Get Next Line Project

This project is an assignment given to students at 42 school. The project acts as a file reader and reads one line from the file on each call.

Installation

To clone the project, use the following command:


git clone https://github.com/cankirkgz/get_next_line.git

Usage

The get_next_line() function is used to read a line from the file. The function takes the file descriptor and a character string as parameters. The read line is returned as a character string.

#include "get_next_line.h"
#include <fcntl.h>

int main()
{
    int fd = open("file.txt", O_RDONLY);
    char *line;

    while (get_next_line(fd, &line) > 0)
    {
        printf("%s\n", line);
        free(line);
    }
    return 0;
}

License

This project is licensed under the MIT License. See the LICENSE file for more information.
