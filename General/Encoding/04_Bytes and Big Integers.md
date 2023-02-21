# **#Bytes and Big Integers**

-   Ta thấy đề cho 1 số lớn như sau:
    data=11515195063862318899931685488813747395775516287289682636499965282714637259206269

-   Để giải mã được số lớn này, ta cần phải dùng thư viện sau:
'''
    from Crypto.Util.number
'''
-   Và dùng câu lệnh **long_to_bytes()** để decode (Ngoài ra, khi bạn muốn encode 1 đoạn byte b'' thì ta sẽ dùng câu lệnh *bytes_to_long()*)

-    Đoạn code sẽ như sau:
```
    from Crypto.Util.number import*

    data=11515195063862318899931685488813747395775516287289682636499965282714637259206269

    flag=long_to_bytes(data).decode()

    print(flag)
```
-    Và cờ của bài này là: ***crypto{3nc0d1n6_4ll_7h3_w4y_d0wn}***


