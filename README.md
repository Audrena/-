# -
判断表中某列数据是否在另一列中
##判断一列是否在另一列中
#方法一：实际工作a/b列有较多数据，
a = [1, 2, 3]
b = [2,3]  
d = [False for c in b if c not in a]
if d:
  print "a不包含b的所有元素"
else:
  print "a包含b的所有元素"

'''
#此方法，可看有多少个b在a中
c=[]
for i in b:
    if i in a:
        c.append(1)
    else:
        c.append(0)
'''
#方法二：数据量较少可使用
a = [1,2,3,4,5,6]
b = [2,4,6]
set(b) < set(a) # a是否包含b，<= 则表示是否是子集
