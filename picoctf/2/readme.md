## Today 30 March
Just changed the if condition

- [ ] The challenge was to get the flag from the *level1.py* and *level1.flag.txt.enc* . By mechanism *level1.py* decrypted the *level1.flag.txt.enc* to display flag.

### PREVIOUS

```python
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
```


### AFTER
```python
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( "1e1a"  == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), 'le1a')
        print(decryption)
        return
    print("That password is incorrect")
```

- [x]  Hence easily got the flag: picoCTF{545h_r1ng1ng_fa343060}
