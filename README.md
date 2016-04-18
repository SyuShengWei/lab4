(A)
0000000000600a30 B __bss_start
0000000000600a30 b completed.6971
0000000000600a20 D __data_start
0000000000600a20 W data_start
00000000004004a0 t deregister_tm_clones
0000000000400520 t __do_global_dtors_aux
00000000006007e8 t __do_global_dtors_aux_fini_array_entry
0000000000600a28 D __dso_handle
00000000006007f8 d _DYNAMIC
0000000000600a30 D _edata
0000000000600a38 B _end
0000000000400644 T _fini
0000000000400540 t frame_dummy
00000000006007e0 t __frame_dummy_init_array_entry
00000000004007d8 r __FRAME_END__
0000000000600a00 d _GLOBAL_OFFSET_TABLE_
                 w __gmon_start__
0000000000400664 r __GNU_EH_FRAME_HDR
0000000000400418 T _init
00000000006007e8 t __init_array_end
00000000006007e0 t __init_array_start
0000000000400650 R _IO_stdin_used
                 w _ITM_deregisterTMCloneTable
                 w _ITM_registerTMCloneTable
00000000006007f0 d __JCR_END__
00000000006007f0 d __JCR_LIST__
                 w _Jv_RegisterClasses
0000000000400640 T __libc_csu_fini
00000000004005d0 T __libc_csu_init
                 U __libc_start_main@@GLIBC_2.2.5
00000000004005c0 T main
00000000004004e0 t register_tm_clones
0000000000400470 T _start
0000000000600a30 D __TMC_END__
0000000000400594 T _Z7averageif
0000000000400566 T _Z7averagePdRd

由下列兩行得知
0000000000400594 T _Z7averageif
0000000000400566 T _Z7averagePdRd
同時具有兩個同為average的函數
因此g++編譯會將他們以參數名稱區隔
if的意思是參數為int 和 float
PdRd是指 pointer double 和 reference double

(B)
1	8
4	8
4	8
8	8

a 是 char  大小為 1byte
b 是 int   大小為 4bytes
c 是 float 大小為 4bytes
d 是 double大小為 8bytes

而 pa pb pc pd 都是pointer
因此大小都為8bytes