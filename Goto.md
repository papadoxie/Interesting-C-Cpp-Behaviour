# Goto

## Goto for jumping between functions
It is possible to jump between functions with goto

#### Example
```C
#include <stdio.h>
#include <stdlib.h>

void *global_label = NULL;

void unreachable()
{
	printf("How did I get here?\n");
}

void set_label()
{
	volatile int scam = 0;
	global_label = &&label;

	printf("Global Label: %p\n", global_label);

	if (scam)
	{
	label:
		unreachable();
	}
}

int main(void)
{
	set_label();
	goto *global_label;
	return 0;
}
```