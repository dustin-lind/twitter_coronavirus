# Coronavirus twitter analysis

**Background Description of Project**

In this project, I scanned all geotagged tweets sent it 2020 to monitor the spread of references to the COVID-19 pandemic on social media by language and location. For context, approximately 500 million tweets are sent everyday, and of those tweets, about 1% are geotagged. 

To analyze the tweets, I followed the MapReduce procedure, which is a famous approach for large scale parallel processing. It is a 3 step procedure summarized in the following image:

<img src=mapreduce.png width=100% />

**Methodology**

I had two goals for this project:

1. To count the number of mentions of a set of hashtags related to the COVID-19 pandemic by commonly used languages (e.g. English, Spanish, Mandarin, etc.)

2. To count the number of mentions of a set of hashtags related to the COVID-19 pandemic by countries (e.g. The United States, United Kingdom, China, etc.)

The hashtags that I tracked were the following:
```
hashtags = [
    '#코로나바이러스',  # korean
    '#コロナウイルス',  # japanese
    '#冠状病毒',        # chinese
    '#covid2019',
    '#covid-2019',
    '#covid19',
    '#covid-19',
    '#coronavirus',
    '#corona',
    '#virus',
    '#flu',
    '#sick',
    '#cough',
    '#sneeze',
    '#hospital',
    '#nurse',
    '#doctor',
    ]
```

**Results**

You can find the detailed breakdown of the number of mentions of each hashtag by country and language in the visualization directory of my repository.

To access a breakdown of hashtags by language, look in the following directory: `viz/lang/`

Additionally, to access a breakdown of hashtags by country, look in the following directory: `viz/country/`

A snapshot of what you would see if you were looking for the number of mentions of `#corona` by country looks as follows:
```
US : 265932
IN : 157067
GB : 80275
TR : 57257
ES : 47660
BR : 41702
DE : 41121
IT : 40929
AR : 31965
NL : 30351
```

Conversely, a snapshot of what you would see if you were looking for the number of mentions of `#hospital` by language looks as follows:
```
en : 41168
es : 3912
und : 2177
in : 913
pt : 589
tl : 271
ca : 271
th : 266
hi : 178
fr : 178
```

Oracle provides a table of all the commonly used [Country and Language Codes](https://docs.oracle.com/cd/E13214_01/wli/docs92/xref/xqisocodes.html)
