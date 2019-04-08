# ABTesting-withAggregatesInPandas
This CodeCademy project uses aggregate measures in Pandas to analyze data and help a company select the best performing ad in an AB test. There are two different versions of an ad, which have been placed in emails and banner ads on Facebook, Twitter, and Google. The company wants to know how the two ads are performing on each platform on each day of the week. 

Before manipulating the data, I inspect the first few lines of the initial dataframe. 
<img width="795" alt="AB1" src="https://user-images.githubusercontent.com/46868984/55711717-939a6080-59ed-11e9-9665-6bbe281bf2a3.png">


Next I use .groupby() and .count() to show the number of ad clicks that came from each UTM source
<img width="794" alt="AB2" src="https://user-images.githubusercontent.com/46868984/55711886-f1c74380-59ed-11e9-9468-e26e9661df31.png">


I then create a new column that will indicate if the ad is clicked as a boolean value. If the value is True, then the ad was clicked.  
Next, I pivot the table so it is easier to analyze the data. 
<img width="790" alt="AB3" src="https://user-images.githubusercontent.com/46868984/55712284-c133d980-59ee-11e9-8893-ab803d44b0d5.png">


After pivoting the table, I add new column to more clearly show the percent of users that clicked each add from each UTM source

<img width="788" alt="AB4" src="https://user-images.githubusercontent.com/46868984/55712571-461ef300-59ef-11e9-8c30-06146d49b67d.png">



To better understand the numbers in the table, I used .groupby() and .count() to show the count of users in each experimental group (A & B). I found that there are 827 users in each group. Next I sorted input from each group into False or True where True indicates that the ad was clicked on
<img width="795" alt="AB5" src="https://user-images.githubusercontent.com/46868984/55713341-bed27f00-59f0-11e9-852c-ce91f9852867.png">


To analyze the AB test, I initialized two new databases that contain only the information from each group. After that I created tables to clearly show how each test performed on each day of the week. 
<img width="796" alt="AB6" src="https://user-images.githubusercontent.com/46868984/55713792-b3cc1e80-59f1-11e9-9f19-c440af610bab.png">


By examining both sets of data, one can see that clicks for ad A is higher on every day of the week except for Tuesday, so overall, A is the better ad.
