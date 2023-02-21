# **#ASCII**

-    Ta thấy đề cho 1 list các số nguyên như sau:
    [99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]
-    Ta nhận ra đây chính là các mã ASCII và ta cần phải đổi chúng về các kí tự chữ trong bảng chữ cái bằng lệnh *chr()* của Python
-    Đoạn code sẽ như sau:
```
    lst=[99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]
    flag=""
    for i in lst:
        flag =flag+chr(i)
    print(flag)
```
-    Và cờ của bài này là: ***crypto{ASCII_pr1nt4bl3}***
