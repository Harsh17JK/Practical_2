# Practical_2
Practical_2

File: /home/ubuntu/practical2dsl.py Page 1 of 1
#playing cricket badminton and football
def intersection(l1,l2):
res = []
for student in l1:
if student in l2:
res.append(student)
return res
def union(l1,l2):
res = l2.copy()
for student in l1:
if not student in l2:
res.append(student)
return res
def diff(l1,l2):
res = []
for student in l1:
if not student in l2:
res.append(student)
return res
a = [1,2,3,4,5,6,7]
b = [2,3,6,7,9,10]
c = [2,4,6,8,10,12]
print(f"A ={a} \nB ={b} \nC ={c} \n")
print(f"a.{intersection(a,b)}")
# # print(union(a,b))
# print(diff(a,b))
print(f"b.{diff(union(a,b), intersection(a,b))}")
# print(union(diff(b,a),intersection(a,b)))
# print(union(diff(b,a),diff(a,b)))
print(f"c.{diff(diff(c,b),a)}")
print(f"d.{diff(union(a,c),b)}")
################################################################
Output : -
ubuntu@ubuntu-Vostro-460:~/DSL$ /bin/python3 /home/ubuntu/DSL/Practical2.py
A =[1, 2, 3, 4, 5, 6, 7]
B =[2, 3, 6, 7, 9, 10]
C =[2, 4, 6, 8, 10, 12]
a.[2, 3, 6, 7]
b.[9, 10, 1, 4, 5]
c.[8, 12]
d.[4, 8, 12, 1, 5]
