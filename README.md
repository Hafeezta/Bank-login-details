# Python 

import random

database = {}

def init():
    isValidoptionselected = False
    print('Welcome to our Jaiz Bank')
    
    while isValidoptionselected ==False:
        haveAccount = int(input('Do you have account with us: 1 (Yes) 2 (No) \n'))
        
        if(haveAccount == 1):
            isValidoptionselected =True
            login()
            
        elif(haveAccount == 2):
            isValidoptionselected =True
            print(register())
        else:
            print('selected invalid option')
         

def login():
    print(' Login to your Account')
    email2 = input("Enter your Email:")
    passw = input('Enter your password')
    if email2 in database and database[email2] == passw:
      print('login successfully') 

    bankoperation()


    
def register():
    print('*******Register********')
    email= input("Enter your Email Address:\n")
    first_Name= input('Enter your first name:\n')
    last_Name= input('Enter your last name:\n')
    password= input('create a password:\n')
    
    AccountNumber = generateAccountNumber()
    
    database[AccountNumber] = [first_Name,last_Name,email,password]

    print("Your Account has been Created")
    
    login()
    
def bankoperation():
  print('some operations')
    

def generateAccountNumber():
    
    return random.randrange(1111111111,9999999999)
    print(generateAccountNumber())
    
init()
