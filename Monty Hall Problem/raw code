'''
#Monty Hall Problem Simulation
#There are three doors, behind one of which is a prize, and behind the other two is not a prize
#We choose 1 random door of 3
#One of the prize-less doors are revealed
#We may stick with or change our choice of door (the prize door being either the one we picked, or the other un-revaled door)
#Doors open and we either win or lose
'''

''' Simulating Monty Hall with Loops:'''

from numpy import random
 
n = 1000000 # number of times to simulate the game-show

#Create 3 doors, behind only one of which is a car (Car = 1, goat/no prize = 0)
#Perform an initial shuffle for better randomness :)?
doors = [0, 1, 0]
random.shuffle(doors)

# These Monty-Hall-Problem-Simulating-Functions return their win counts (with_switching and without_switching)
# so we can to compare the efficacy of using a door-switching strategy vs staying on your originally picked door

def monty_hall_switching(n, doors):
    with_switching = 0 
    for i in range(n):
        random.shuffle(doors) #doors are randomized at start of each iteration of the game show
        pick = random.randint(3)
        picked_door = doors[pick] #contestant picks 1 of 3 doors at random (doors[0], [1], [2])
        for i in range(len(doors)):
            if doors[i] == 0 and i != pick: #Reveal a prizeless/0 door which is not the one we picked
                revealed_door = i
                #print('test', revealed_door)
        for i in range(len(doors)):
            if i != pick and i != revealed_door: #We change to the other remaining door
                if doors[i] == 1 :
                    with_switching += 1 #If the switch causes a win, add to the win count, else play again  (to n iterations)                      
    return with_switching
    
def monty_hall_without_switching(n, doors):
    without_switching = 0  
    for i in range(n):
        pick = random.randint(3)
        #print('pick=',pick)
        picked_door = doors[pick] #contestant picks 1 of 3 doors at random (doors[0], [1], [2])
        #print('door=',picked_door)
        if picked_door == 1: 
            without_switching += 1 #If we picekd right, we win! Else, play again (to n iterations)
    return without_switching

#Run the simulations both ways to update win counters of each strategy. Using n = 10000 iterations gives us the expected
# 33% no switch win rate, and 66% switching win rate. 

switch_wins = monty_hall_switching(n, doors)
no_switch_wins =  monty_hall_without_switching(n, doors)
 
print('Without switching, we won',no_switch_wins, 'of', n,'games')
print('With switching, we won',switch_wins, 'of', n,'games')
print('Sticking to our original door, we won', 100 * no_switch_wins / n, '% of the time, while switching doors we won', 100 * switch_wins / n, '% of the time')
##########################################################################################################################


''' Now the same thing without loops: '''
#I still have to loop over each iteration of the game being played, but I can cut out loops used within each iteration

#Create counts of wins for our no-loop monty-hall functions    
switch_wins2 = 0
no_switch_wins2 = 0  

def monty_hall_switching2(doors):
    random.shuffle(doors)
    picked_door = random.choice(doors)    
    if picked_door == 1:   #if you pick the car right away and plan to switch - you've lost
        return 0
    else:    # if you didn't choose the car initially, you chose the goat - so you'd switch to the car and win
        return 1

def monty_hall_without_switching2(doors):
    random.shuffle(doors)
    picked_door = random.choice(doors)    
    if picked_door == 1:   #if you pick the car right away and don't switch - you win
        return 1
    else:    # if you didn't choose the car initially, you chose the goat - so you lost
        return 0

# I only use this loop here - hopefully that's what you had in mind :)
for i in range(n):
    no_switch_wins2 += monty_hall_without_switching2(doors)
    switch_wins2 += monty_hall_switching2(doors)

print('\nSame results without loops in the code:')
print('Without switching, we won',no_switch_wins2, 'of', n,'games')
print('With switching, we won',switch_wins2, 'of', n,'games')
print('Sticking to our original door, we won', 100 * no_switch_wins2 / n, '% of the time, while switching doors we won', 100 * switch_wins2 / n, '% of the time')

#Clearly, switching is the best strategy. 
#Although mathematically, it is far
