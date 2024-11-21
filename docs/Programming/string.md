```c
char *strcpy(char *to, const char *from)
{
	char *save = to;

	for (; (*to = *from); ++from, ++to);
	return save;
}
```


```c
int strcmp(const char *s1, const char *s2)
{
	while (*s1 == *s2++)
		if (*s1++ == '\0')
			return 0;
	return (*(const unsigned char *)s1 - *(const unsigned char *)(s2 - 1));
}
```


```c
size_t strlen(const char *str)
{
	const char *s;

	for (s = str; *s; ++s);
	return (s - str);
}
```


```c
char *strchr(char *p, int ch)
{
	for (;; ++p) {
		if (*p == ch)
			return p;
		if (!*p)
			return (char *)NULL;
	}
	/* NOTREACHED */
}
```
