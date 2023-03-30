## Today 30 March
Just changed the if condition

### PREVIOUS
'''
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")
'''

### AFTER
'''
def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( "1e1a"  == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), 'le1a')
        print(decryption)
        return
    print("That password is incorrect")
'''

##### Hence easily got the flag: picoCTF{545h_r1ng1ng_fa343060}
