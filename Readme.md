# 彈幕 Python 應用至網頁上

一時興起寫的，教學/娛樂性質居多，我可能也不會想要維護。！！

## 想法來源：
![](https://i.imgur.com/KWdbCVB.png)

## 目標網站：https://tlk.io/
![](https://i.imgur.com/zKY9VFI.png)

# 構想：
在上課途中，有人有問題的話就能在 tlk.io 上提問，即時在 ppt 上面發射彈幕，好處是 tlk.io 是匿名的，壞處是還沒做垃圾字過濾。

# 結果圖

![](./img/demo.gif)


順便打個廣告，未來再把這個東西的投影片(心路歷程！？)放上來。


## [FB:台科大電腦研習社](https://www.facebook.com/ntustcc/)

# 目前結果
- 某些網站可用 (不包含 Google Slides / Microsoft Slides)
- pdf 可用(請使用瀏覽器打開pdf的方式！)


# 需求
- python 3.5 up
- jupyter notebook
- [selenium](https://pypi.org/project/selenium/)
- [Web Driver(Chrome)](https://sites.google.com/a/chromium.org/chromedriver/downloads)

# 現在作法
用 Python Selenium 開兩個瀏覽器
- tlk.io 偵測是否有人輸入文字(每三秒去讀一次) 
- 使用瀏覽器打開投影片 - 透過 Selenium 執行 js 輸入彈幕

# 使用方法 - 整理中（有些 Code 還是寫死的）


=> 使用 Pdf 版本
> 使用 jupyter notebook 打開 tlk_danmu.ipynb
>
> 找到下面兩行，換成你要的網址
> ![](https://i.imgur.com/JUwje1J.png)
> 
> 然後一直 run 應該就行了。
> 
=> 使用 iframe 版本(Google Slides)
> 使用 jupyter notebook 打開 tlk_danmu-with-iframe.ipynb
>
> 首先打開 Google Slides
>
>
>
> 找到下面兩行，換成你要的網址
> ![](https://i.imgur.com/JUwje1J.png)
> 
> 然後一直 run 應該就行了。
> 




# 各種條件測試
- [X] 使用 Selenium 讓 js 的腳本可正常生成 - Successed
    https://pypi.org/project/selenium/
- [X] 使用 Chrome 開啟 pdf 使用 - Successed
- [X] 在 Slideshare 上使用 - Successed
- [X] 使用 Google slides 的 iframe  - Failed
- [ ] 使用 Requests.get - tlk.io - Failed
    結果如下：https://pastebin.com/02EyXYG3
- [ ] 在 Google slides 上使用 - Failed
- [ ] 在 Microsoft slides 上使用 - Failed


# 未來方向
- [ ] 使用 Google slides 的 iframe 目前不能全螢幕
- [ ] 朝向 javascript 去做爬蟲，現在開兩個 Selenium driver 真的很奇怪呢
- [ ] 想在 Google/Microsoft slides 使用 
- [ ] 可能丟在 Line chatbot 串接，剛好和社團課程銜接。



# Thanks
Borrow heavily from [jquery.danmu.js](https://github.com/chiruom/jquery.danmu.js)
https://templated.co/industrious
