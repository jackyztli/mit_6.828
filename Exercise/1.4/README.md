Build pointer.c  
gcc -Wall -g -o pointer pointer.c

The result is :  
1: a = 0x7fffe7473ec0, b = 0x55710195e260, c = 0xf0b5ff
2: a[0] = 200, a[1] = 101, a[2] = 102, a[3] = 103
3: a[0] = 200, a[1] = 300, a[2] = 301, a[3] = 302
4: a[0] = 200, a[1] = 400, a[2] = 301, a[3] = 302
5: a[0] = 200, a[1] = 128144, a[2] = 256, a[3] = 302
6: a = 0x7fffe7473ec0, b = 0x7fffe7473ec4, c = 0x7fffe7473ec1  

my machine is : Linux jacky 4.15.0-55-generic #60-Ubuntu SMP Tue Jul 2 18:22:20 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux


