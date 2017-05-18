# Linked list
Each node has a value, and a pointer to the next node

## Singly linked list:
```c++
struct ll;
struct ll
{
	int val;
	ll *next;
}
```

This memory map:
```
addr val next | addr val next | addr val next | addr val next |
1200   3 1208 | 1208  12 1224 | 1216   7 null | 1224   5 1216 |
```
corresponds to:
3->12->5->7

## Doubly linked list:
```c++
struct ll;
struct ll
{
	int val;
	ll *next;
	ll *prev;
}
```

## Circular lined list:
Singly linked list where the last element links to the first element

### Q. Find the nth last node in a linked list
O(n), O(1) space Solution:
```
Move pointer a to n+1th element
Move pointer b to 0th element
keep incrementing both till a is at the last element
pointer b has l-nth element
```