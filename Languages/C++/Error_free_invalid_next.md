##### <div style="color:#369">问题起源</div>

&ensp;&ensp;&ensp;&ensp;在图片处理中的对加水印图和原图的频域相互做残差时，运行出现错误

```shell
└─[134] *** Error in `/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3': free(): invalid next size (normal): 0x00000000011bf620 ***
 ======= Backtrace: =========
/lib/x86_64-linux-gnu/libc.so.6(+0x777e5)[0x7f1e2a2037e5]
/lib/x86_64-linux-gnu/libc.so.6(+0x7fe0a)[0x7f1e2a20be0a]
/lib/x86_64-linux-gnu/libc.so.6(cfree+0x4c)[0x7f1e2a20f98c]
/usr/local/lib/libopencv_core.so.3.2(_ZN2cv3Mat10deallocateEv+0xc9)[0x7f1e2ad0a8b9]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3(_ZN2cv3Mat7releaseEv+0x4f)[0x405d1f]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3(_ZN2cv3MatD1Ev+0x18)[0x405b24]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x408665]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x40825a]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x407c12]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x406d7b]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3(_ZNSt6vectorIN2cv3MatESaIS1_EED1Ev+0x36)[0x406416]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x4043a4]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x404a91]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x4050d8]
/lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0xf0)[0x7f1e2a1ac830]
/mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3[0x402189]
======= Memory map: ========
00400000-0040e000 r-xp 00000000 08:04 664586                             /mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3
0060e000-0060f000 r--p 0000e000 08:04 664586                             /mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3
0060f000-00610000 rw-p 0000f000 08:04 664586                             /mnt/D/Developer/WorkPlace/Personal-Workplace-Temp/Algorithm/C++/WaterMark/bin/ff2t3
00e3b000-01375000 rw-p 00000000 00:00 0                                  [heap]
7f1e1c000000-7f1e1c021000 rw-p 00000000 00:00 0
7f1e1c021000-7f1e20000000 ---p 00000000 00:00 0
7f1e20c46000-7f1e21cec000 rw-p 00000000 00:00 0
7f1e21cec000-7f1e21cf2000 r-xp 00000000 08:01 2097758                    /usr/lib/x86_64-linux-gnu/libdatrie.so.1.3.3
7f1e21cf2000-7f1e21ef2000 ---p 00006000 08:01 2097758                    /usr/lib/x86_64-linux-gnu/libdatrie.so.1.3.3
7f1e21ef2000-7f1e21ef3000 r--p 00006000 08:01 2097758                    /usr/lib/x86_64-linux-gnu/libdatrie.so.1.3.3
7f1e21ef3000-7f1e21ef4000 rw-p 00007000 08:01 2097758                    /usr/lib/x86_64-linux-gnu/libdatrie.so.1.3.3
7f1e21ef4000-7f1e21f17000 r-xp 00000000 08:01 2097435                    /usr/lib/x86_64-linux-gnu/libgraphite2.so.3.0.1
7f1e21f17000-7f1e22116000 ---p 00023000 08:01 2097435                    /usr/lib/x86_64-linux-gnu/libgraphite2.so.3.0.1
7f1e22116000-7f1e22118000 r--p 00022000 08:01 2097435                    /usr/lib/x86_64-linux-gnu/libgraphite2.so.3.0.1
7f1e22118000-7f1e22119000 rw-p 00024000 08:01 2097435                    /usr/lib/x86_64-linux-gnu/libgraphite2.so.3.0.1
7f1e22119000-7f1e2211e000 r-xp 00000000 08:01 2101116                    /usr/lib/x86_64-linux-gnu/libXdmcp.so.6.0.0
7f1e2211e000-7f1e2231d000 ---p 00005000 08:01 2101116                    /usr/lib/x86_64-linux-gnu/libXdmcp.so.6.0.0
7f1e2231d000-7f1e2231e000 r--p 00004000 08:01 2101116                    /usr/lib/x86_64-linux-gnu/libXdmcp.so.6.0.0
7f1e2231e000-7f1e2231f000 rw-p 00005000 08:01 2101116                    /usr/lib/x86_64-linux-gnu/libXdmcp.so.6.0.0
7f1e2231f000-7f1e22321000 r-xp 00000000 08:01 2104349                    /usr/lib/x86_64-linux-gnu/libXau.so.6.0.0
7f1e22321000-7f1e22521000 ---p 00002000 08:01 2104349                    /usr/lib/x86_64-linux-gnu/libXau.so.6.0.0
```


##### <div style="color:#369"> 造成该问题的原因 </div>

&ensp;&ensp;&ensp;&ensp;此错误是由内存错误, 可能造成这个问题的原因

+ 用`free()`释放, 没有`malloc()`分配内存的指针
+ 用`delecte()`删除一个没有被`new`创建的对象
+ 重复用`free()/delete()`方法释放指针内存或者删除对象
+ 内存溢出
+ 相关内存不能访问

