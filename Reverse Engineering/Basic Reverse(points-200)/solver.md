We just have to reverse this 
```c 
  for (local_10 = 0; local_10 < 8; local_10 = local_10 + 1) {
    local_9 = flag.txt[local_10];
    fputc((int)local_9,local_28);
  }
  for (local_14 = 8; (int)local_14 < 23; local_14 = local_14 + 1) {
    if ((local_14 & 1) == 0) {
      local_9 = flag.txt[(int)local_14] + 5;
    }
    else {
      local_9 = flag.txt[(int)local_14] + -2;
    }
    fputc((int)local_9,local_28);
  }
