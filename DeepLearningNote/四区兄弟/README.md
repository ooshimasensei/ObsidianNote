# Deep Solar Eye Dataset

Image files names contains the time of the day and %age power_loss of the panel with respect to the clean panel and irradiance level.
These informations can be used for regression. 
For Example:
solar_Wed_Jun_28_7__5__6_2017_L_0.0123268698061_I_0.0566274509804.jpg
can be parsed as - 
solar_day_Month_date_hour__minute__second__year_L_%ageloss_I_irradiancelevel.jpg

solar_Fri_Jun_16_6__0__25_2017_L_0.0901960784314_I_0.003
  0      1   2   3   4     6     8   10 11 -3          -1
solar_周_月_日_时__分__秒__年_L_损失_I_辐照度等级
solar_Fri_Jun_16_6__0__25_2017_L_0.0901960784314_I_0.003

s=[时，分，秒，辐照度，损失]  
L=pvpl=[损失]                               label.npy
R=enF= [时，分，秒，辐照度]     feats.npy
    pim=[图片名集合]                     
I=[imread后的图片集合]               image.npy
