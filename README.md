*** multiple csv to dataFrame ***

---
'''python
#i!/usr/bin/python
import pandas as pd
'''
윗코드는 파이썬의 일부
'''sh
npm -1 jupyter-drawio
'''
윗코드는 주파이터 그림그리는 익스텐션.


---
'''python
#!/usr/bin/python
import os
import pandas as pd'''
윗 코드는 파이썬의 일부
'''

os.chdir('/root/Downloads/jupyter/data')
''' 
윗코드는 path내 자식 받기.
'''
results = pd.DataFrame([])
for counter, file in enumerate(glob.glob("GSM*")):
    namedf=pd.read_csv(file, skiprows=0 ,sep='\t' )
    results=results.append(namedf)
'''
윗코드는 자식내 GSM을 포함하는 csv파일을 만들어서 각각의 df로 변환하여 results라는 df로 합산한다.
'''
'''
results.to_csv('./data.csv ')
''' 
합산한 df를 csv 파일로 저장함.


---
2018-03-07

'''
pd.concat((pd.read_csv(f,sep='\t') for f in all_files),axis=1)
''' 
윗코드는all_files내 있는 f를 read_csv를 사용하여 sep='\t'인 pd로 변환시킨다.axis=1은 '열'추가

---
