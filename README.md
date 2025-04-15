# flames-games
def flames_game(a,b):
    flames=['FRIENDS','LOVE','AFFECTION','MARRAIGE','ENEMY','SISTER']
    
    a=a.replace(" ","").lower()
    b=b.replace(" ","").lower()

    for char in a:
        if char in b:
            a=a.replace(char,"",1)
            b=b.replace(char,"",1)
           
            
    length=len(a+b)
    

    index=0
    while len(flames)>1:
        index=(index+length-1)%len(flames)
        flames.pop(index)
    return flames[0]

a=input("enter a first name : ")
b=input("enter a second name : ")
result=flames_game(a,b)
print(result)
