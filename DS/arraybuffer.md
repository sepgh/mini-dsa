# ArrayBuffer

We still rely on an `array` but we do not use `0` as our head and `length - 1` as our tail. Anything outside the head and tail is `null`.

Now, if we want to append to the array we just increase our tail by 1 and write into that index. This makes append (and prepend) to have constant time without need of growth (well, till some point).


## RingBuffer

If we take array buffer and apply `tail % length` to it, the tail can go even behind the head.


In both ArrayBuffer and RingBuffer you'd still need to increase the capacity at some point which would be `O(N)` operation (most likely).


## More info
https://frontendmasters.com/courses/algorithms/arraybuffer/


