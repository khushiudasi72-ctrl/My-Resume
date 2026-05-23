#RESTAURANT ORDER MANAGEMENT SYSTEM
menu={'pizza':250,'burger':120,'pasta':180,'cold drink':60}
total_bill=0
item_total=0
price=0
quantity=0
total_bill=0
while True:
    print('------------------WELCOME TO KHUSHI RESTAURANT--------------------')
    print('1.Show Menu')
    print('2.Ask item name')
    print('3.Calculate')
    print('4.Exit')
    ch=int(input('enter your choice : '))
    if ch==1:
        print(menu)
    elif ch==2:
        item=input('enter your item : ')
        if item in menu:
            price=menu[item]
            quantity=int(input('enter your quantity'))
            more=input('Do you want to order more darling (yes/no) ?')
            if more=='yes':
                print(menu)
                item=input('enter your item :')
                if item in menu:
                    price=menu[item]
                    quantity=int(input('enter your quantity :'))
            else:
                print('OKAY ! ENJOY YOUR MEAL SIR/MAM')
        else:
            print('SORRY! This item does not exist in our restaurant') 
    elif ch==3:
        item_total= price*quantity
        total_bill+=item_total
        print(f'YOUR TOTAL BILL IS : {total_bill}')
    elif ch==4:
        print('BYE BYE ! COME AGAIN')
        break 
