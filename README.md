# Production-Planning-Problem
Python code of Integer program to get optimal value in production planning problem
Problem statement: The demand for a product in the next 12 months is provided in Table 1.  Operating duringregular  hours,  the  production  capacity  is  800  units/month.   But  overtime  capacity  is  an  additional  200units/month. The selling price is the same irrespective of production mode, and the unit production costsare $10 and $12 for regular time production and overtime production, respectively. In addition, there existsa storage cost of $1 per unit per month for each unsold unit held over.  Also, the inventory is perishable,and each unit can be held for at most two more months beyond the month in which it is produced.




Mathematical model:Parameters:
number of months in planning horizon=12
j denotes the type of production modes (regular-j=1, over-time-j=2)
di denotes the demand in month i = 1,…,12; 
uj denotes monthly production capacity limits for j =1,2; u1=800 unit ,u2=200 unit.
cj denotes unit production cost for type j =1,2; c1=$10 per unit,c2=$12 per unit
h denotes unit storage cost per month=$1/month

Decision Variables:
Xijk denotes the number of units of type j produced (regular or overtime)in month i and sold in month k, where i = 1,…….,12; j = 1,2; k = 1,…12. Here,

Linear Model:
Objective Function:
Min      ∑_(j=1)^2▒Cj ∑_(i=1)^12▒〖∑_(k=1)^12▒Xijk    〗+ ∑_(j=1)^2▒∑_(i=1)^12▒∑_(k=1)^12▒〖h(k-i)Xijk 〗   
Subject to:
Xijk=0 if k<i or k>i+2 for i=1,..12  j=1,2    k=1,…12
∑_(j=1)^2▒∑_(i=1)^12▒〖Xijk 〗 = dk    for  k = 1,2,3,….12
∑_(k=1)^12▒Xijk ≤ uj for  j=1, 2
Xijk ≥ 0  ∀   i = 1,…..,12; j = 1,2; k = i,..,i+2.
