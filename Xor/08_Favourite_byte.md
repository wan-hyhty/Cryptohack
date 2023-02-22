# **#Favourite byte**
-   Đề cho ta 1 đoạn mã hexa data='73626960647f6b206821204f21254f7d694f7624662065622127234f726927756d' 
-   Ta phải unhexlify đoạn data này và ra được 1 đoạn bytes
-   Ta chuyển đoạn này qua max Ascii và được một list num
-   Tiếp theo, ta xor từng phần tử trong list num với các số từ 0 --> 255 (mình hông biếc giải thích sao lại thế :v)
-   Khi thu được các list gồm các bytes thì ta có thêm 1 lệnh
        ```if "crypto" ``` // nếu là kí hiệu mật mã thì ...
-   Đoạn code sẽ như sau:
```
    from binascii import unhexlify

    string = unhexlify("73626960647f6b206821204f21254f7d694f7624662065622127234f726927756d")
    print(string)
    num = []
    for i in string:
        num.append(i)

    for i in range(256):
        print(i)
        flag=[]
        for j in num:
            flag.append(chr(i^j))
        a=''.join(flag)
        if "crypto" in a:
            print(a)
```

-   Và cờ của bài này là: ***crypto{0x10_15_my_f4v0ur173_by7e}***
