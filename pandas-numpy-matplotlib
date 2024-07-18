# ----------------------- P A N D A S ----------------------- #
import pandas as pd
import numpy as np
#-------------
'''
a=['a','b','c']
no=[1,2,3]
ser=pd.Series(no,a)
print(ser)
'''
# and try this - see how the index changes
'''
a=['a','b','c']
no=[1,2,3]
ser=pd.Series(a,no)
print(ser)
'''
#--------------
#
# N A N ( for nan both pandas and numpy has to be imported as nan is an attribute of numpy )
'''
a= [1,np.NAN,3]
ser=pd.Series(a)
print(ser)
'''
# Range and index used within series
'''
s= pd.Series(range(1,15,3),index=[x for x in 'abcde'])
print(s)
'''
# indexing, sclicing , and accesing data 

s=pd.Series([1,2,3,4,5],index=['a','b','c','d','e'])
print(s[0]) #prints the first element as the index of first element is 0
print(s[:3]) #prints the first 3 elements 
print(s[-3:])#prints the last 3 elements 

# ---- I L O C & L O C ----#
'''
s=pd.Series([1,2,3,4,5],index=['a','b','c','d','e'])
print(s.iloc[1:4])#output starts from index no 1 and ends at index no3 
print(s.loc['b':'e'])#output starts from element b and ends at element e . it includes both b and e
''' 
'''
# creating series from scalar values fron consatnt values
ser=pd.Series(55,index=['a','b','c','e'])
print(ser) # when data is a scalar value it is a MUST to provide index
'''
# creating series with loop
'''
s=pd.Series(range(1,15,3),index=[x for x in 'abcde'])
print(s)
'''
#creating a series from dictionary 
'''
ser=pd.Series({'jan':31,'feb':28,'mar':31,'apr':30})
print(ser)
'''
# naming a series and it's index 
'''
series=pd.Series({'jan':31,'feb':28,'mar':30,'apr':31})
series.name= 'days' #naming series 
series.index.name='month' #naming index
print(series)
'''
#creating series using mathematical expression
'''
s=np.arange(10,15)
print(s)#  creating the base for mathematical function
series1=pd.Series(index=s,data=s*4) # doing the operaation on it 
print(series1) 
series2=pd.Series(index=s,data=s**2) 
print(series2) 
'''

#series attributes .... pg 3.16
'''
ser=pd.Series(range(1,15,3),index=[x for x in 'abcde'])
print(ser.index)
print(ser.values)
print(ser.shape)
print(ser.size)
print(ser.hasnans)
print(ser.empty)
'''
# head and tail
''' 
ser=pd.Series([*range(10,51,10)],index=[x for x in 'abcde'])
print(ser)
print(ser.head())# by default it's first 5 values 
print(ser.head(2)) 
print(ser.tail())
print(ser.tail(2))
'''
# mathematical operations 
'''
s=pd.Series(np.arange(11,15))
print(s)
s1=pd.Series(np.arange(21,25))
print(s1)
s2=pd.Series(np.arange(21,25),index=[*range(101,105)])
print(s+s1)
print(s*s1)
print(s/s1)
print(s+s3) 
'''
# vector operations
'''
s=pd.Series(np.arange(11,15))
print(s+2)
print(s*3)
print(s**2)
print(s>13)
'''
# retrieving values using conditions 
'''
s=pd.Series(np.arange(50,101,10))
print(s)
print(s<70) #returns true or false 
print(s[s<70]) #returns values less than 70 
'''
#deleting elements from series 
'''
s=pd.Series(np.arange(1,10))
print(s.drop(3))
print(s)
''' 
#--------------------D A T A F R A M E S ----------------------# 
#creating df from list
# 1st way
''' 
list1=[10,20,30,40]
df1=pd.DataFrame(list1)
print(df1)
'''
#2nd way 
'''
lst=[['sreya',20],['rak',22],['sri',18]] #notice the brackets 
df=pd.DataFrame(lst,columns=['name','age'])
print(df)
'''
#creating from series 
'''
#notice in output there is no need to specify index 
marks=pd.Series({'vijay':80,'raj':92,'meg':67,'rad':95,'sha':97})
age=pd.Series({'vijay':32,'raj':28,'meg':30,'rad':25,'sha':20})
df=pd.DataFrame({'Marks':marks,'Age':age})
print(df)
'''
#sorting data using boolen 
'''
marks=pd.Series({'vijay':80,'raj':92,'meg':67,'rad':95,'sha':97})
age=pd.Series({'vijay':32,'raj':28,'meg':30,'rad':25,'sha':20})
df=pd.DataFrame({'Marks':marks,'Age':age})
print(df)

print(df.sort_values(by=['Marks'])) 
#sorting the data on the basis of a column 

print(df.sort_values(by=['Marks'],ascending = False))# sorted in on the basis of desending order of marks 
'''
#creating from dictionary 
'''
#notice the brackets 
#nan cannot be used without importing numpy
#notice that the values of the column conataing nan has changed to float values 
stu={'rik':[67,77,88],'ritu':[78,58,np.NaN],'AJ':[75,87,67],'Pan':[88,65,74],'ad':[92,np.NaN,70]}
stud=pd.DataFrame(stu)
print(stud)
'''
#selecting and accesing from dataframe

#selecting and accesing from dataframe
'''
stu={'rik':[67,77,88],'ritu':[78,58,np.NaN],'AJ':[75,87,67],'Pan':[88,65,74],'ad':[92,np.NaN,70]}
stud=pd.DataFrame(stu)
print(stud)

print(stud[0:2])#0st to 1rd rows
'''

#to create an index
'''
stu={'rik':[67,77,88],'ritu':[78,58,np.NaN],'AJ':[75,87,67],'Pan':[88,65,74],'ad':[92,np.NaN,70]}
stud=pd.DataFrame(stu)
print(stud)

df=pd.DataFrame(stu,index=['sno1','sno2','sno3'])
print(df)
'''
# set index and reset index
'''
marks=pd.Series({'vijay':80,'raj':92,'meg':67,'rad':95,'sha':97})
age=pd.Series({'vijay':32,'raj':28,'meg':30,'rad':25,'sha':20})
df=pd.DataFrame({'Marks':marks,'Age':age})
print(df)

df.set_index('Marks',inplace=True)

print(df) 

df.reset_index(inplace=True)
'''
# ---------------column---------------#

#renaming a column in datframe
'''
stu={'rik':[67,77,88],'ritu':[78,58,np.NaN],'AJ':[75,87,67],'Pan':[88,65,74],'ad':[92,np.NaN,70]}
stud=pd.DataFrame(stu)
#print(stud)

#notice the brackets used as well as the ' : '
df=stud.rename(columns={'rik':'rick'}) #changed name from rik to rick 
print(df)
'''
################################
####### adding a column #######
'''
df['age2']=45 #new col with scalar val
df['age3']=pd.Series([42,44,50])#new col using list
df['tot age']=df['age2'] + df['age3'] #new col by calculation
#print(df)

df['tot age']=df['tot age']+ 10
df['updated age']=df['tot age'] #replacing column or renaming a column

print(df)
### selecting column from df ### pg 3.29

print(df['tot age'])
print(df.iloc[:,[0,3]]) # all rows and the 0th and 3rd  column
print(df.iloc[[1,2],[0]]) # 1st and 2nd row of 0th column
print(df.iloc[:,0:4])# all rows of 0,1,2,3 columns 

# deleting a column from df #pg 3.29

#using  del

del df['updated age']
print(df)

#using pop
df.pop('age3')
print(df)

#using drop
df.drop('age2',axis=1) # NOT WORKING CHECK AGAIN
print(df)
'''
#############################

# binary operations
'''
student1={'unit 1 ':[5,6,8,3,10],'unit2':[7,9,6,6,15]}
df1=pd.DataFrame(student1)

student2={'unit 1 ':[3,3,6,6,8],'unit2':[5,9,8,10,5]}
df2=pd.DataFrame(student2)

print(df1)
print(df2)

print(df1.sub(df2)) # df1 - df2
print(df1.rsub(df2)) #df2 - df1
print(df1.add(df2)) #df1 + df2
print(df1.radd(df2))# df2 + #df1
print(df1.mul(df2)) #multiplication
print(df1.div(df2)) #division ...df1 divided by df2 
'''
#### NAN & FILLNA ####
'''
a=([2,5,6,7,8],[8],[10,14],[5,8,9])
df=pd.DataFrame(a)
print(df)

print(df.fillna(8)) # filling all the missing values with 0

print(df.fillna({1:-10,2:-5})) #1st col nans are replaced by -10 and 2nd col nans ar replaced by -5

print(df.fillna(method='ffill')) #nans are replced by the value of the cell above 
'''
### concat
###
# STATICS
lst=[['sreya',20,24],['rak',22,78],['sri',18,56]] #notice the brackets
df=pd.DataFrame(lst,columns=['name','age','score'])
print(df)

print(df.max()) #displays the max value in each column
print(df.min()) #displays the min value in each column
print(df['age'].max()) # displays the max value in age column

print(df['score'].sum())#displays the sum of the given col --- .sum() skips the nan values by defalut
print(df['score'].sum(skipna=True))# now it does not skip nan values

print(df['name'].count())
