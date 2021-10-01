# Desck-Calculator
def addOak():
     # add extra cost for oak wood
     oakWood = (500 * 0.2)+ 500
     return oakWood
def addDraws (n):
    # add cost of draws - R80 per draw
    # number of draws is past as a parameter
     draws = n * 80
     return draws
def calcDisc (Tot):
    # add extra cost for oak wood 
     disc = 0.05 * Tot
     return disc
# get customer's requests
typeWood = input ("would you like the wood to be oak? Y/N  ")
includeDraws = input ("would you like draws included with the desk? Y/N  ")
# calculate costs of each item 
basicCost = 500
if (typeWood == "Y"):
     woodCost = addOak()
else:
     woodCost = 0  
if (includeDraws == "Y"):
     numDraws = int (input ("How many draws would you like?  "))
     drawCost = addDraws(numDraws)
else:
     drawsCost = 0         
# find total cost
totCost = basicCost + woodCost + drawCost
# check for discount
if totCost < 650:
     discRec = calcDisc(Tot)
else:
     discRec = 0
# calculate final cost and print
finalCost = totCost - discRec
print (finalCost)           
