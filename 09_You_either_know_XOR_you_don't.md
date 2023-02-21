# **#You either know, XOR you don't**
-   Để Xor nhanh và tiện lợi hơn thì mình dùng thư viện pwn và import xor, tuy nhiên cần phải đổi sang bytes
    ```from pwn import xor```

-   Đề bài cho ta 1 đoạn mã Hexa 
    data='0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104'

-   Ta cần chuyển mã này sang Bytes
        data=bytes.fromhex(data)

-   Ngoài ra, ta thấy dạng của cờ là: 
        string = b'crypto{'
    Ta đoán là key sẽ là kết quả của xor data với string
    Và kết quả của phép xor là: b'myXORke+y_Q\x0bHOMe$~seG8bGURN\x04DFWg)a|\x1dTM!an\x7f'
    Và ta đoán key là: key=b'myXORkey'

-   Cuối cùng, ta chỉ cần xor key với data, ta sẽ tìm được flag

-   Đoạn code sẽ như sau:
```
    from pwn import xor

    data=bytes.fromhex('0e0b213f26041e480b26217f27342e175d0e070a3c5b103e2526217f27342e175d0e077e263451150104')
    string=b'crypto{'
    print(xor(data,string))

    key=b'myXORkey'
    print(xor(key,data).decode())
```

-   Và cờ của bài này là: ***crypto{1f_y0u_Kn0w_En0uGH_y0u_Kn0w_1t_4ll}***
