# ***#HEX***

-    Ta thấy đề bài cho 1 đoạn string:
     `63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d'
     
-    Ta nhận thấy đây chính là 1 đoạn mã Hexa (Tìm hiểu thêm tại đây: [https://en.wikipedia.org/wiki/Hexadecimal])

-    Ta cần chuyển mã này qua Bytes bằng câu lệnh: *bytes.fromhex(data).decode()* 

-    Đoạn code sẽ như sau:
```
    `data='63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d'
     flag=bytes.fromhex(data).decode()
     print(flag)
```
     
-    Và cờ của bài này là: ***crypto{You_will_be_working_with_hex_strings_a_lot}***