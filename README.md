# Playing-with-list-in-python-
#Finding the a mean and median 
niversities = [
['California Institute of Technology', 2175, 37704],
['Harvard', 19627, 39849],
['Massachusetts Institute of Technology', 10566, 40732],
['Princeton', 7802, 37000],
['Rice', 5879, 35551],
['Stanford', 19535, 40569],
['Yale', 11701, 40500]
]
def enrollement_stats(n):
    """Forming a new list from niversities"""
    enrollement_value=[]
    tuition_fee=[]
    for n in niversities:
         enrollement_value.append(n[1])
         tuition_fee.append(n[2])
    return enrollement_value,tuition_fee
enrollement=enrollement_stats(niversities)
print(enrollement)
def mean(enrollement):
    """Finding the mean of enrollement list"""
    y=1
    for n in enrollement:
        addition=sum(n)/len(n)
        print(f"The mean of list {y} is:{addition:,.2f}")
        y+=1
    return addition
mean(enrollement)
def median(enrollement):
    """Finding the median of enrollement list"""
    y=1
    for n in enrollement:
        n.sort()
        index=int(len(n)/2)
        print(f"The median of  list {y} is {n[index]}")
        y+=1
    return n[index]
median(enrollement)
print(f"Total student {sum(enrollement[0]):,}")
print(f"Total tuition ${sum(enrollement[1]):,}")
