# Mask-identification
口罩即時辨識系統

該系統為一套即時辨識是否戴口罩之系統，其功能就像疫情時代進出公共場合會看到的辨識系統，只是筆者將該想法利用簡單的CNN模型訓練配合電腦攝像頭來呈現。

筆者製作這套系統時目的為期末專題，所以目前這樣的程度個人認為非常適中，報告的時間好抓，主題很新穎，貼近生活又用到新穎技術，製作時間也不需要太長(雖然筆者花了很多時間找資料XD，很符合一個期末小專題的程度。)
因此個人認為這項專案很適合從未碰過深度學習，學過python想玩一些進階的結合，很有興趣想做AI但手邊沒有適合訓練資料的人。希望這項專題可以給找不到期末專題的學生一個方向

![image](https://user-images.githubusercontent.com/43988698/215306956-51aba0ee-16ee-469b-b923-069f151eebba.png)

*_該系統利用自行蒐集資料，搭建模型訓練，並結合opencv調用攝像頭，建立一套即時辨識是否有戴口罩的系統。但由於資料量少、模型簡單、訓練資料單純，因此該系統要上市仍有一定的難度。_*

# 資料蒐集
想做AI深度學習，一定會需要大量的資料，但有時大量資料不好找，找到的也不一定好訓練(筆者曾去kaggle上抓口罩資料下載後做訓練，也試過爬蟲去爬網路上口罩照片做訓練，但效果實在慘不忍睹XD)。因此筆者採用錄影的方式蒐集資料，錄影可以想像成很多很多照片結合起來的一個檔案，那理所當然將這些檔案全部拆開後就可以得到所有的圖片，而這些圖片正好適合拿來當作訓練的資料。而錄影的話也不需要用手機錄，直接用電腦的攝像頭錄即可(這麼做會遇到畫素的問題，後續討論會提到)
以下為戴口罩與沒戴口罩訓練圖片範例
![new_mask1091](https://user-images.githubusercontent.com/43988698/215305427-a61ed116-59fd-4e3c-8c31-abe3f96a8981.jpg)
![new_mask1196 (2)](https://user-images.githubusercontent.com/43988698/215305443-612d7f12-bdb4-4bf8-81a8-396ee45270db.jpg)

# 模型訓練
筆者做這項專案時是大三下，那時經濟能力不是太好，硬體設備僅有一台i5筆電不可能在本地端實施訓練，不過還好GOOGLE有提供colab供使用者免費顯卡使用，因此筆者是在colab底下開發。

由於訓練的資料十分簡單只是一堆性質很近的照片(同一部影片拍出來的畫質光照雜質環境那些都很像)，因此模型的部分不用到很複雜，筆者僅用幾層CNN的模型來訓練這些資料，即可獲得不錯成果。高達98%的正確率~

不過再次強調，這筆訓練成果，訓練資料單純、模型簡單、資料量少，所以出來結果是絕對經不起考驗的，也就是說當我今天拿個不同的攝像頭或換個人來測正確率就會掉很多，因此筆者才會說這僅是一個很簡單很簡單的辨識系統，只是為了期末專題而產生，一方面報告時的變數比較好抓，一方面這樣的難度才剛好符合短短幾個月甚至幾個禮拜的時間。

# 聯繫我
如果有任何問題歡迎聯絡我 e-mail:t1616joy@yahoo.com.tw / t1616joey1@gmail.com
