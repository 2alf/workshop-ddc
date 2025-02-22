### intern decompiler
```c
int foo(int x) {
  return x^0x20;
}
```

### junior decompiler

```c
int foo(int x, int y) {
  if (x < y) {
      return y;
  } else {
      return x;
  }
}
```

### middle decompiler

```c
int foo(int x) {
  int y = 0;
  while (y <= 4) {
      x += 2;
      y += 1;
  }
  return x;
}
```