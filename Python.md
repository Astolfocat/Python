# Python
（一些用Python写的杂七杂八的东西，记录在此）
1. 下面是在整理阿福的图片的时候，因为强迫症想要给图片同一名字，但是手动重命名过于麻烦，现在既然学了Python那么也是该让它发挥价值了（yeah~）
因为比较简单所以就不做批注了叭
```python
# coding = gbk
import  os
import sys

path = 'F:\\Pictures\\photogallery\\Astolfo\\'
file_names = os.listdir(path)
n = 0
for name in file_names:
    oldname = path+file_names[n]
    newname = path+'Astolfo_'+str(n+1).zfill(3)+'.jpg'
    os.rename(oldname, newname)
    print(oldname,'--->',newname)
    n+=1
