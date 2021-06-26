# Ramu-Nathipam
# Goodies
d={'fitbit Plus':7980,'IPods':22349,'MI Band':999,'Cult Pass':2799,'Macbook Pro':229900,'Digital Camera':11101,'Alexa':9999,'Sandwich Toaster':2195,'Microwave Oven':9800,'Scale':4999}
values=list(d.values())
values.sort()
n=int(input())
SUM=values[-1]
for i in range(len(values)-n+1):
    Sub_list=[]
    Sub_list=values[i:i+n]
    if((Sub_list[-1]-Sub_list[0])<SUM):
        SUM=Sub_list[-1]-Sub_list[0]
        Final=Sub_list
print("Number of the employees: {}".format(n))
for result in Final:
    for key,value in d.items():
        if(result==value):
            print("{}: {}".format(key,value))
print("And the difference the chosen goodie with highest price and lowest price is {}".format(SUM))
