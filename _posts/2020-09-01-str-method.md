---
layout: post
title: >
    strlen(), strcpy(), strcmp() 구현
categories: [C]
tags: [C]
---

<span style="color:red">**\*str1 = str1의 주소값 = 포인터가 가리키는 주소에 저장된 값이라고 하겠습니다.**</span>

# strlen()

### 함수 원형
```c
size_t strlen(const char* str)
```

문자열을 받아서 해당 문자열의 길이를 반환하는 함수입니다.  

### 구현
```c
int strlen(const char *str)
{
	int count;

	count = 0;
	while (*str) //*str = '\0'
	{
		str++;
		count++;
	}
	return (count);
}
```

문자열 str의 주소를 받아 주소값이 null이 될 때까지 카운트하며 포인터를 넘기고 카운트한 값을 리턴합니다.

    str = a b c d e \0
    point *
    count = 0
    ...while
    str = a b c d e \0
    point           *
    count = 5

<br/>
<br/>

# strcpy()  

### 함수 원형  
```c
char* strcpy(char* dest, const char* origin);
```

origin에 있는 문자열 전체를 dest로 복사를 하는 함수 입니다.  

### 구현
```c
char	*strcpy(char *dest, char *origin)
{
	char *temp;

	temp = dest;

	while (*origin)
	{
		*dest = *origin;
		origin++;
		dest++;
	}
	*dest = '\0'; // null
	
	return (temp);
}
```

origin과 dest의 주소를 받아 temp에 dest의 주소를 넣고  

dest의 주소값에 origin의 주소값을 origin의 주소값이 null을 가르킬 때까지 넣습니다.  

문자열의 마지막에는 null값이 들어갑니다.  

temp의 주소를 리턴합니다.  

    origin = a b c d e \0
	point    *
    dest   = a
	point    *
    temp   = a
	point    *

	origin = a b c d e \0
	point      *
    dest   = a b
	point      *
    temp   = a b
	point    *
    ...while
    origin = a b c d e \0
	point              *
    dest   = a b c d e \0
	point              *
    temp   = a b c d e \0
	point    *

	return temp

<br/>
<br/>

# strcmp()

### 함수원형
```c
int strcmp(const char* str1, const char* str2)
```

두개의 문자열을 비교 하여 문자열이 완전히 같다면 0을 반환하고, 다르면 음수 혹은 양수를 반환하는 함수입니다.  

### 구현  
```c
int	strcmp(const char *str1, const char *str2)
{
	while (*str1 || *str2)
	{
		if (*str1 != *str2)
			return (*str1 > *str2 ? 1 : -1);
		str1++;
		str2++;
	}
	return (0);
}
```

str1과 str2의 주소를 받아 두 주소값을 비교합니다.

만약 두 주소값이 다르다면 ascii 코드상에서 두 주소값을 비교합니다.  

str1의 주소값이 더 크면 1  

str2의 주소값이 더 크면 -1 을 리턴합니다.  

만약 두 문자가 같다면 str1과 str2의 포인터를 넘깁니다.  

두 주소값이 모두 null을 가르키면 두 문자열은 같다는 뜻으로 0을 리턴합니다.  

	str1 = a b c d \0
	str2 = a b c d e \0
	
	str1 = a b c d \0
	point  *
	str2 = a b c d e \0
	point  *
	...while
	str1 = a b c d \0
	point          *
	str2 = a b c d e \0
	point          *

	return -1