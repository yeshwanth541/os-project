#include <assert.h>
#include <limits.h>
#include <math.h>
#include <stdbool.h>
#include <stddef.h>
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>


char* readline();
char** split_string(char*);
// Complete the catAndMice function below.
//  remember to make sure the string static or allocate on the heap. for example,
// static char str[] = "hello world";
// return str;
//
// OR
//
// char* str = "hello world";
// return str;
//

char* catAndMice(int x, int y, int z) {
}
int main()
{
FILE* fptr = fopen(getenv("OUTPUT_PATH"), "w");

char* q_endptr;
char* q_str = readline();
int q = strtol(q_str, &q_endptr, 10);

if (q_endptr == q_str || *q_endptr != '\0') { exit(EXIT_FAILURE); }

for (int q_rep = 0; q_rep < q; q_rep++) {
char** xyz = split_string(readline());

char* x_endptr;
char* x_str = xyz[0];
int x = strtol(x_str, &x_endptr, 10);

if (x_endptr == x_str || *x_endptr != '\0') { exit(EXIT_FAILURE); }

char* y_endptr;
char* y_str = xyz[1];
int y = strtol(y_str, &y_endptr, 10);

if (y_endptr == y_str || *y_endptr != '\0') { exit(EXIT_FAILURE); }

char* z_endptr;
char* z_str = xyz[2];
int z = strtol(z_str, &z_endptr, 10);

if (z_endptr == z_str || *z_endptr != '\0') { exit(EXIT_FAILURE); }

char* result = catAndMice(x, y, z);

fprintf(fptr, "%s\n", result);
}
fclose(fptr);
return 0;
}

char* readline() {
size_t alloc_len = 1024;
size_t data_len = 0;
char* data = malloc(alloc_len);

while (true) {
char* cursor = data + data_len;
char* line = fgets(cursor, alloc_len - data_len, stdin);

if (!line) { break; }

data_len += strlen(cursor);

if (data_len < alloc_len - 1 || data[data_len - 1] == '\n') { break; }

size_t new_length = alloc_len<< 1;
data = realloc(data, new_length);

if (!data) { break; }
alloc_len = new_length;
}
if (data[data_len- 1] == '\n') {
data[data_len - 1] = '\0';
}
data = realloc(data, data_len);
return data;
}
char** split_string(char* str) {
char** splits = NULL;
char* token = strtok(str, " ");

int spaces = 0;

while (token) {
splits = realloc(splits, sizeof(char*) * ++spaces);
if (!splits) {
return splits;
}

splits[spaces - 1] = token;

token = strtok(NULL, " ");
}

return splits;
} 
