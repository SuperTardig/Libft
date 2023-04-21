# Libft
The Goal of this 42 school project is to recreate a number of the C standard library and create some other functions. These functions will help me for the rest of my time in my at 42 Québec. We needed to understand how the C standard library worked internally to be able to faithfully recreate them.

# Mandatory
The mandatory functions we needed to recreate where has followed:

  - int ft_isalpha(int c): This function takes an int, which is the ascii representation of a char, and returns 1 if it is a letter and 0 if it isn't
  - int ft_isdigit(int c): This function follows the same principle has ft_isalpha, but returns 1 if it is a number
  - int ft_isalnum(int c): This function follows the same principle has ft_isalpha, but returns 1 if it is a number or letter
  - int ft_isascii(int c): This function follows the same principle has ft_isalpha, but returns 1 if it is in the range of ascii
  - int ft_isprint(int c): This function follows the same principle has ft_isalpha, but return 1 if c is able to be printed
  - size_t ft_strlen(char *str): A simple function that takes a char* and returns it's lenght
  - void *ft_memset(void *b, int c, size_t len): This function takes a void*, an int and a size_t, it sets the value of each index of b to c for len
  - void ft_bzero(void *s, size_t n): This function takes a void* and a size_t, it sets the value of each index of s to NULL for n
  - void *ft_memcpy(void *dst, const void *src, size_t n): This fucntion takes two void* and a size_t, it copies the value of each index of src to dst for n
  - void *ft_memmove(void *dst, const void *src, size_t n): This function takes and does the same thing as ft_memcpy while being more cautious of overlapping memory
  - size_t ft_strlcpy(char *dst, const char *src, size_t dstsize): This function takes two char* and a size_t, it copies src into dst for dstsize
  - size_t ft_strlcat(char *dst, const char *src, size_t dstsize): This function takes two char* and a size_t, it concatenate src into dst for dstsize
  - int ft_toupper(int c): This function takes an int, which is the ascii representation of a char, and return the uppercase version if it is a letter
  - int ft_tolower(int c): This function takes an int, which is the ascii representation of a char, and return the lowercase version if it is a letter
  - char *ft_strchr(const char *s, int c): This functions takes a char* and an int, it finds c in s and returns the adress of the first occurence
  - char *ft_strrchr(const char *s, int c): This funcitons follows the same principle has ft_strchr, except it returns the last occurence
  - int ft_strncmp(const char *s1, const char *s2, size_t n): This functions takes two char* and a size_t it compares s1 to s2 for n and returns the difference between the first index that doesn't match
  - void *ft_memchr(const void *s, int c, size_t n): This functions follows the same principle as ft_strchr, execpt it works with void*
  - int ft_memcmp(const void *s1, const void *s2, size_t n): This functions follows the same principle as ft_strncmp, execpt it works with void*
  - char *ft_strnstr(const char *haystack, const char *needle, size_t len): This function take two char* and a size_t, it find needle in haystack for len and returns the adress of the first characther of needle in haystack
  - int ft_atoi(const char *str): This function takes a char* and then converts it tries to convert it to an int
  - void *ft_calloc(size_t count, size_t size): This function takes two size_t, it allocates memory for count by size and set each value to NULL
  - char *ft_strdup(const char *s1): This function take char* and creates a copy which it the returns
  - char *ft_substr(char const *s, unsigned int start, size_t len): This functions takes a char*, an unsigned int and a size_t, it creates a char* from s at start for len
  - char *ft_strjoin(char const *s1, char const *s2): This functions takes two char*, it create a new char* by concatenating s2 to s1
  - char *ft_strtrim(char const *s1, char const *set): This function takes two char*, it create a new char* by removing the chars in set from the start and end of s1 until it find a char not present in set
  - char **ft_split(char const *s, char c): This function takes a char* and a char, it creates a char** by splitting s each times it find c
  - char *ft_itoa(int n): This function takes an int, it creates a char* which is n in char representation
  - char *ft_strmapi(char const *s, char (*f)(unsigned int, char)): This function takes a char* and a function pointer, it creates a new char* by applying f to each element of s
  - void ft_striteri(char *s, char (*f)(unsigned int, char)): This functions follows the same principle as ft_strmapi, execpt it doesn't create a new char* and directly modifies s
  - void ft_putchar_fd(char c, int fd): This functions takes a char and an int, it writes c on fd 
  - void ft_putstr_fd(char *s, int fd): This functions follows the same principle as ft_putchar_fd, except it writes a char*
  - void ft_putendl_fd(char *s, int fd): This functions follows the same principle as ft_putchar_fd, except it writes a char* and a newline
  - void ft_putnbr_fd(int n, int fd):  This functions follows the same principle as ft_putchar_fd, except it writes an int
  
 # Bonus
 There were also some functions that could be completed has a bonus. These fucntions used a list struct named t_list. They are has followed:
 
  - t_list *ft_lstnew(void *content): This function takes a void*, it creates a new list node from content
  - void ft_lstadd_front(t_list **lst, t_list *new): This function takes a t_list** and a t_list*, it adds new to the front of lst
  - int ft_lstsize(t_list *lst): This function takes a t_list*, it finds the size of the list and returns it
  - t_list *ft_lstlast(t_list *lst): This function take a t_list*, it finds the last node of the list and returns it
  - void ft_lstadd_back(t_list **lst, t_list *new): This function follows the same principle as ft_lstadd_front, except it adds it to the back
  - void ft_lstdelone(t_list *lst, void (*del)(void *)): This function takes a t_list* and a function pointer, it deletes the content of lst using del
  - void ft_lstclear(t_list **lst, void (*del)(void *)): This function takes a t_list** and a function pointer, it deletes the lst and every node following using del
  - void ft_lstiter(t_list *lst, void (*f)(void *)): This fuction takes a t_list* and a function pointer, it applies f to every node in lst
  - t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *)): This function takes a t_list* and two function pointer, it creates a new t_list* from using f on every node in lst and it uses del to delete the old node in lst
  
  
  # Usage
  To use this library, you need to:
  1. Clone this repository
  2. Go to the root of the repository and use `make` (if you want to use the bonus, run `make bonus`)
  3. Include `libft.h` in your project
  4. Link the library at compile time by adding `-L./libft -lft` to your compilation line
