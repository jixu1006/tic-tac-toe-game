#Python assignment2 TIC TAC TOE GAME
#Author: Ji Xu
#Date: 11 June 2017


import random
board=[' ',' ',' ',
       ' ',' ',' ',
       ' ',' ',' ']

def print_board():
    print(" ","1"," ","2"," ","3")
    print('1',board[0],'|',board[1],'|',board[2])
    print('---','+---+','---')
    print('2',board[3],'|',board[4],'|',board[5])
    print('---','+---+','---')
    print('3',board[6],'|',board[7],'|',board[8])

def checkLine(char,spot1,spot2,spot3):
    if board[spot1]==char and board[spot2]==char and board[spot3]==char:
        return True

def checkWin(char):
    if checkLine(char,0,1,2):
        return 0
    if checkLine(char,3,4,5):
        return 0
    if checkLine(char,6,7,8):
        return 0
    if checkLine(char,0,3,6):
        return 0
    if checkLine(char,1,4,7):
        return 0
    if checkLine(char,2,5,8):
        return 0
    if checkLine(char,0,4,8):
        return 0
    if checkLine(char,2,4,6):
        return 0

def player1_step():

    print('\nplayer1 please go~~~\n')

    input_row=input('Please select a row number:')
        
    while input_row !='1' and input_row !='2' and input_row !='3':
        print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
        input_row=input('Please select a row number:')
        
        
    input_column=input('Please select a column number:')
    
    while input_column !='1' and input_column !='2' and input_column !='3':
        print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
        input_column=input('Please select a column number:')

    while True:

        if input_row=='1' and input_column=='1' and board[0]!='o'and board[0]!='x':
            board[0]='x'
            print_board()
            break;
        elif input_row=='1' and input_column=='2' and board[1]!='o'and board[1]!='x':
            board[1]='x'
            print_board()
            break;
        elif input_row=='1' and input_column=='3' and board[2]!='o'and board[2]!='x':
            board[2]='x'
            print_board()
            break;
        elif input_row=='2' and input_column=='1' and board[3]!='o'and board[3]!='x':
            board[3]='x'
            print_board()
            break;
        elif input_row=='2' and input_column=='2' and board[4]!='o'and board[4]!='x':
            board[4]='x'
            print_board()
            break;
        elif input_row=='2' and input_column=='3' and board[5]!='o'and board[5]!='x':
            board[5]='x'
            print_board()
            break; 
        elif input_row=='3' and input_column=='1' and board[6]!='o'and board[6]!='x':
            board[6]='x'
            print_board()
            break;
        elif input_row=='3' and input_column=='2' and board[7]!='o'and board[7]!='x':
            board[7]='x'
            print_board()
            break;
        elif input_row=='3' and input_column=='3' and board[8]!='o'and board[8]!='x':
            board[8]='x'
            print_board()
            break;
        else:
            print('This place is taken!!!')
            input_row=input('Please select a row number:')
            while input_row !='1' and input_row !='2' and input_row !='3':
                print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
                input_row=input('Please select a row number:')
            input_column=input('Please select a column number:')
            while input_column !='1' and input_column !='2' and input_column !='3':
                print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
                input_column=input('Please select a column number:')
            
def player2_step():
    
    print('\nPlayer2 please go~~~\n')
        
    input_row=input('Please select a row number:')
        
    while input_row !='1' and input_row !='2' and input_row !='3':
        print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
        input_row=input('Please select a row number:')
        
        
    input_column=input('Please select a column number:')
    
    while input_column !='1' and input_column !='2' and input_column !='3':
        print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
        input_column=input('Please select a column number:')

    while True:
        if input_row=='1' and input_column=='1' and board[0]!='o'and board[0]!='x':
            board[0]='o'
            print_board()
            break;                             
        elif input_row=='1' and input_column=='2' and board[1]!='o'and board[1]!='x':
            board[1]='o'
            print_board()
            break;
        elif input_row=='1' and input_column=='3' and board[2]!='o'and board[2]!='x':
            board[2]='o'
            print_board()
            break;
        elif input_row=='2' and input_column=='1' and board[3]!='o'and board[3]!='x':
            board[3]='o'
            print_board()
            break;
        elif input_row=='2' and input_column=='2' and board[4]!='o'and board[4]!='x':
            board[4]='o'
            print_board()
            break;
        elif input_row=='2' and input_column=='3' and board[5]!='o'and board[5]!='x':
            board[5]='o'
            print_board()
            break;               
        elif input_row=='3' and input_column=='1' and board[6]!='o'and board[6]!='x':
            board[6]='o'
            print_board()
            break;               
        elif input_row=='3' and input_column=='2' and board[7]!='o'and board[7]!='x':
            board[7]='o'
            print_board()
            break;
        elif input_row=='3' and input_column=='3' and board[8]!='o'and board[8]!='x':
            board[8]='o'
            print_board()
            break;                 
        else:
            print('This place is taken!')
            input_row=input('Please select a row number:')
            while input_row !='1' and input_row !='2' and input_row !='3':
                print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
                input_row=input('Please select a row number:')
            input_column=input('Please select a column number:')
            while input_column !='1' and input_column !='2' and input_column !='3':
                print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
                input_column=input('Please select a column number:')




#main function starts
print('\n~~~Welcome To TIC TAC TOE GAME!~~~\n')
choose=input("--Do want to play with person or computer?\n--Choose person enter 'p'-- Choose computer enter 'c'." )
while choose!='p' and choose!='c' and choose!='P' and choose!='C':
    print('\nPay attention!!Please enter "p" or "c"!!\n')
    choose=input("--Do want to play with person or computer?\n--Choose person enter 'p'-- Choose computer enter 'c'." )


#person vs. person
if choose=='P' or choose=="p":
    print("\nYou will play with person~~\n(There is a situation of nobody wins. When you meet this situation , don't be panic and you can open this game again to try more.)")
    print_board()
    player=input('\nPlease choose "X" or "O" , "X" will go first\n')
    while player!='X' and player!='O' and player!='x' and player!='o':
            print('\nPay attention!!Please enter"X"or"O"!!\n')
            player=input('Please choose "X" or "O"~~:')
            
    step_count=0

    if player=='X'or player=='x':
        print('\nYou are player1~~~You can go first~~~')
        while True:
            step_count=step_count+1
            player1_step()
            if checkWin('o')==0:
                print('Player2 win!!!!\nGame Over~~~')
                break;
            elif checkWin('x')==0:
                print('Player1 win!!!!\nGame Over~~~')
                break;
            elif step_count==9 and checkWin('o')!=0 and checkWin('x')!=0:
                print('\n~~~Draw~~~')
                break;
            
            step_count=step_count+1
            player2_step()
            if checkWin('o')==0:
                print('Player2 win!!!!\nGame Over~~~')
                break;
            elif checkWin('x')==0:
                print('Player1 win!!!!\nGame Over~~~')
                break;
            elif step_count==9 and checkWin('o')!=0 and checkWin('x')!=0:
                print('\n~~~Draw~~~')
                break;
    elif player=='O' or player=='o':
        print('\nYou are player2~~~Let player1 go first~~~')
        
        while True:
            step_count=step_count+1
            player1_step()
            if checkWin('o')==0:
                print('Player2 win!!!!\nGame Over~~~')
                break;
            elif checkWin('x')==0:
                print('Player1 win!!!!\nGame Over~~~')
                break;
            elif step_count==9 and checkWin('o')!=0 and checkWin('x')!=0:
                print('\n~~~Draw~~~')
                break;
            
            step_count=step_count+1
            player2_step()
            if checkWin('o')==0:
                print('Player2 win!!!!\nGame Over~~~')
                break;
            elif checkWin('x')==0:
                print('Player1 win!!!!\nGame Over~~~')
                break;
            elif step_count==9 and checkWin('o')!=0 and checkWin('x')!=0:
                print('\n~~~Draw~~~')
                break;


#person vs. computer           
if choose=='c' or choose=="C":
    print("\nYou will play with computer~~\nYour step will show X\n(There is a situation of nobody wins. When you meet this situation , don't be panic and you can open this game again to try more.)")
    print_board()
    a=1
    b=2
    while a<b:
        
        input_row=input('Please select a row number:')
            
        while input_row !='1' and input_row !='2' and input_row !='3':
            print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
            input_row=input('Please select a row number:')
            
            
        input_column=input('Please select a column number:')
        
        while input_column !='1' and input_column !='2' and input_column !='3':
            print('\nPay attention!!Please enter 1 or 2 or 3!!\n')
            input_column=input('Please select a column number:')
            

        if input_row=='1' and input_column=='1' and board[0]!='o'and board[0]!='x':
            board[0]='x'
            print_board()

            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        
                        print('Computer win!!!!')
                        a=3
                    break;
                
        elif input_row=='1' and input_column=='2' and board[1]!='o'and board[1]!='x':
            board[1]='x'
            print_board()

            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                
            
        elif input_row=='1' and input_column=='3' and board[2]!='o'and board[2]!='x':
            board[2]='x'
            print_board()

            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                
        elif input_row=='2' and input_column=='1' and board[3]!='o'and board[3]!='x':
            board[3]='x'
            print_board()
            
            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                          
        elif input_row=='2' and input_column=='2' and board[4]!='o'and board[4]!='x':
            board[4]='x'
            print_board()
            
            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                               
        elif input_row=='2' and input_column=='3' and board[5]!='o'and board[5]!='x':
            board[5]='x'
            print_board()
            
            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                               
        elif input_row=='3' and input_column=='1' and board[6]!='o'and board[6]!='x':
            board[6]='x'
            print_board()
            
            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                
                
        elif input_row=='3' and input_column=='2' and board[7]!='o'and board[7]!='x':
            board[7]='x'
            print_board()
            
            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                

        elif input_row=='3' and input_column=='3' and board[8]!='o'and board[8]!='x':
            board[8]='x'
            print_board()
            
            if checkWin('x')==0:
                print('You win!!!')
                break;

            while True:
                
                computer=random.randint(0,8)
                if board[computer]!='o'and board[computer]!='x':
                    board[computer]='o'
                    print("Your opponent's step")
                    print_board()

                    if checkWin('o')==0:
                        print('Computer win!!!!')
                        a=3
                    break;
                
        else:
            print('This place is taken!')
        

