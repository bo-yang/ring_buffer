# ring_buffer

A circular buffer implemented by std::vector.

Compile `g++ -Wall ring_buffer_test.cc -o ring_buffer`

Expected output for the test program:

```
$ ./ring_buffer 
Initial state:  capacity 8, size 7, head 0, tail 7, not full, elements:
 0 1 2 3 4 5 6
_head = 0, _tail = 7, _size = 7, front: 0, back: 6
1-elem inserted:  capacity 8, size 8, head 0, tail 0, full, elements:
 0 1 2 3 4 5 6 7
2-elem inserted:  capacity 8, size 8, head 2, tail 2, full, elements:
 2 3 4 5 6 7 8 9
2-elem poped:  capacity 8, size 6, head 4, tail 2, not full, elements:
 4 5 6 7 8 9
2-elem inserted:  capacity 8, size 8, head 4, tail 4, full, elements:
 4 5 6 7 8 9 10 11
Resized to 10:  capacity 10, size 8, head 0, tail 8, not full, elements:
 4 5 6 7 8 9 10 11
_head = 0, _tail = 8, _size = 8, front: 4, back: 11
1-elem inserted:  capacity 10, size 9, head 0, tail 9, not full, elements:
 4 5 6 7 8 9 10 11 12
Resized to 6:  capacity 6, size 6, head 0, tail 0, full, elements:
 7 8 9 10 11 12
1-elem inserted:  capacity 6, size 6, head 1, tail 1, full, elements:
 8 9 10 11 12 13
_head = 1, _tail = 1, _size = 6, front: 8, back: 13
```
