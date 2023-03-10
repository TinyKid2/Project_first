from zipimport import zipimporter
import pandas as pd
from collections import Counter
import matplotlib.pyplot as plt
from wordcloud import WordCloud, STOPWORDS 
import math
# 자료가져오기
df1 = pd.read_csv('/Users/stone/programing/python_exercise/code_States/1Week/realdonaldtrump.csv')
#index(['id', 'link', 'content', 'date', 'retweets', 'favorites', 'mentions','hashtags']

# 날짜에서 년도,월 잘라내기
df1['date00'] = df1.date.str.split(' ').str[0] # 올린시간 제외한 column
df1['df1year'] = df1.date00.str.split('-').str[0]
df1['df1month'] = df1.date00.str.split('-').str[1]
# dfday = df2.date00.str.split('-').str[2]


# print(df1.df2year)
# print(df1.df1month)

# 필요한 데이터만 뽑아내기
df2 = df1[['date','content','retweets', 'favorites','df1year', 'df1month']] #

# #데이터 갯수 세기
# df20 = df2['df1year'].value_counts()
# print(df20)

# 데이터 년도별 자르기
df2009 = df2.loc[0:55, :]
df2010 = df2.loc[56:198, :]
df2011 = df2.loc[199:1067, :]
df2012 = df2.loc[1068:5260, :]
df2013 = df2.loc[5261:13463, :]
df2014 = df2.loc[13464:19464, :]
df2015 = df2.loc[19465:27171, :]
df2016 = df2.loc[27172:31116, :]
df2017 = df2.loc[31117:33347, :]
df2018 = df2.loc[33348:36348, :]
df2019 = df2.loc[36349:40938, :]
df2020 = df2.loc[40939:43351, :]

# # favorites 평균들 dict에 저장
favorites_average = {'2009' : round(df2009.favorites.median()),'2010' : round(df2010.favorites.median()),'2011' : round(df2011.favorites.median()),'2012' : round(df2012.favorites.median()),'2013' : round(df2013.favorites.median()),'2014' : round(df2014.favorites.median()),'2015' : round(df2015.favorites.median()),'2016' : round(df2016.favorites.median()),'2017' : round(df2017.favorites.median()),'2018' : round(df2018.favorites.median()),'2019' : round(df2019.favorites.median()),'2020' : round(df2020.favorites.mean()) }
print(favorites_average)

# 그래프로 출력
# myList = favorites_average.items()
# myList = sorted(myList) 
# x, y = zip(*myList) 
# plt.plot(x, y)
# plt.show()
# df2data = Counter(df2.df1year)
# sorted_df2data = sorted(df2data.items())

# print(df2data)
## retweet dict에 저장
retweet_average = {'2009' : round(df2009.retweets.median()),'2010' : round(df2010.retweets.median()),'2011' : round(df2011.retweets.median()),'2012' : round(df2012.retweets.median()),'2013' : round(df2013.retweets.median()),'2014' : round(df2014.retweets.median()),'2015' : round(df2015.retweets.median()),'2016' : round(df2016.retweets.median()),'2017' : round(df2017.retweets.median()),'2018' : round(df2018.retweets.median()),'2019' : round(df2019.retweets.median()),'2020' : round(df2020.retweets.median()) }
print(retweet_average)
# myList = retweet_average.items()
# myList = sorted(myList) 
# x, y = zip(*myList) 
# plt.plot(x, y)
# plt.show()

# text = df2.loc[df2.loc[:,'favorites'].idxmax(),'content']
string1 = [df2.loc[df2009.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2010.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2011.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2012.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2013.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2014.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2015.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2016.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2017.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2018.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2019.loc[:,'favorites'].idxmax(), 'content'],df2.loc[df2020.loc[:,'favorites'].idxmax(), 'content']]
print(string1)
# text = ''.join(v for v in string1)

# wordcloud = WordCloud(width = 600, height = 600, 
#                      ).generate(text) 
  
# # WordCloud 출력                    
# plt.figure(figsize = (4, 4), facecolor = None) 
# plt.imshow(wordcloud) 
# plt.axis("off") 
# plt.tight_layout() 
# plt.show()

