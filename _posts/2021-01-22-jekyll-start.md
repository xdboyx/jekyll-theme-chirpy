---
title: 使用 jekyll 在github上做筆記
date: 2021-01-22 14:00:00 +0800
categories: [jekyll]
tags: [jekyll]
pin: true
---

原本程式筆記是記在Notion上面，不過看到蠻多人在gitgub page上分享筆記

覺得如果自己的筆記也能幫助其他有需要的人，感覺也是蠻不錯。

>[Notion](https://www.notion.so/) 在2020年5月之後，block 就可以無限制的使用

於是在google大神的幫助之下。

發現我們可以使用 **jekyll** 在github上作筆記。。

## [jekyll 官網](https://jekyllrb.com/) 

我們可以看到 DOCS 的 Quick start 的頁面

有需要先安裝 Ruby 相關檔案的說明
![](https://public.boxcloud.com/api/2.0/internal_files/767659731323/versions/819044136300/representations/png_paged_2048x2048/content/1.png?access_token=1!-hv5stCja7KMbiJxR5AJSp_hJGhx6eNU03QTQ7XcLUAUIJhSjMe92GDfK6CjHTWGgKti2vlHArOLAm5kClgePUHygwchPKzo4vWji6PPtM3jirizM6JtUhtqaTe2bUgitrmkOOyY8pl3M7Tif1Iylp3p4q26Xj-5AWdTsRihDeA4XCye3mGK9IYwi0XHXMNP1HTxOYKjMf0DI2ph6gE_h2zk_ri4xHiIV2u77IxWuMsUBaHP0csHCI2MCdcWFX8YH4Ci5YD9yoOsoFvmj2emZ6VVzNk_iYolDSa3jTwyIuHk841asCMPIVBWUBQmtt19920CGwb0EcAR7FffA7D3I5v-WdgWK9cb6jNnL6dPhlREyZjDJnrvU5CYwLC_IipCpVl4ZVIGFP9QSlDhN9vQxWW7gF_LBJSFwMtRG_x2qtysHJFPye4gzuJTyPzsk6HhBRN--_KAhiT7ZPeHUa_BxkqP9TqWRlwmx0vo8ZyDWnIuHJGwm5Es7ao6nNwptolG0xivt0klfL2jlzqRbI09tN4muUqVHNzGm7OcbS5Bdeb2vsu5-9SjhqcWIenL13d_jEYTh4wZ9gCsxe3z0WdKfmiCe7EAkM1MfsuG8l0lSTDQ6DcQTxZj48fmRip23cARruIrV0aIiwffV1tu6rDWU8uKQ8LD5dRQyAVVezKrjA1Itg..&box_client_name=box-content-preview&box_client_version=2.62.0)

點開 [Requirements 看裡面的內容](https://jekyllrb.com/docs/installation/#requirements)

由於我是Windows系統的
![](https://public.boxcloud.com/api/2.0/internal_files/767660888904/versions/819045430104/representations/jpg_paged_2048x2048/content/1.jpg?access_token=1!NXNr2LNEatEsvWtX-WZ_TEJ0W1gDRGK0ajZVx4m0vl_pXaptYpXazGWxHdNcPVUuxqKo2ATno77F9G_9nl2I9ruqdLljzxfgUUQrqmeTPnM6dr3sI_AgvoPd8XD1GoS1SrpizhH0WYjJcZmRvbY8Yen5hJaRsZ2Fclgaw9477fIi9pJjxocd3xl1JwyNTxokRR5W5jOPy3SOTWexi2rPfqm9Ixwke7ufDpNHKy8rmyRf-_1nCpi0Af3ImZ9Drm84SfMF1y2foI9JIALTjN93VcS48VSWydSz1p6cgiD03a8yVkdSvHel6v7TTrWhJwACPfgBHvY1c15AFpPkgrCK-Rzl0erNpk-KoG_Mun0UvVqKdOyaOIQqdAvM4m4yeHhDS9QAfuUF2myxCQ1oPaDjXtrkTGx_5pwrvkwNJHcC0enDmLCkYHllB6ml1LrlE0LAp7RD1mTQyDwiJxvM6c8jm1ecKFzqipR1RxNB-gEKa6mM41H1hhyrgcfOPjSANYEV_iM_lq_V8QlQUl5d8EnIGZFKHR6II4At7QSdRayqJtPSbR7eEOfrn_VK97SE2Ev6ahhYkct04H3t6ShPTYlEaWA93gn61nGnuGb3v41GSnCyOeydTYpoe1gPoALGoiLaxEhxXDdEY4nbo9MzG3fs7AbrO04y5sG9bxCjETx_RghbSw..&box_client_name=box-content-preview&box_client_version=2.62.0)

[點 Windows](https://jekyllrb.com/docs/installation/windows/)

## Install Ruby
在 [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/) 頁面可以看到詳細教學。

大致上的步驟:

1. [Install Ruby](https://rubyinstaller.org/downloads/)
   ![](https://public.boxcloud.com/api/2.0/internal_files/767669694124/versions/819054398524/representations/jpg_paged_2048x2048/content/1.jpg?access_token=1!2kCo6liLnPM9zRVY0aRSnk9aYjXAw2aGaAEpl4rsQS5rll2ayswpOFwg9O3y8jCVDX6TSdCO1f1c_oqu4RUb3jDCXxhuxYmRyPxLCRixFdXlSwur7I1XcD8ud9vXeqXS_rrxfFYMI2oTUiVhaQbzK5S-qsGYUdC8S9lgddYli7_iXPx8lYcoZ2fH1GSI6U_57hZ7TxyCXzgD069y28toOhonaO5VnnqJ8EEzr7o_WWzRSQQq2o8ZZ-_E5qH9wQH3HD2szvFmyCA79tc5NU1wNRrCX699OqEkJGmdjARTxBS5uGvJbF7xp444rKRjCaykvRt6L6T2edFpX7aWCCqDD97aFTtXGgXN12zI2wM4cgsUTGzk0P--coZ5fJodu89tk7uto62I07VI2LzDMlttYHkfB-9MSazdlliK553S70K3uMS0LaZGYhK9WkORdhAGTak0b23a6U8Iz3y4OOl0p36Aw90kaX6TxZAz2h_baWHxXBuFZDqrb-NbHrgmQzzjHTXJ_6eFjNzz15BYUdVtOE3BawSsc8rGsK9x3SGw27Vucq9UuttYMSEhyATRP7KP-kI2gYi894pK3H1CLHSrbNxEvscl4CC3xiPjvjfCvUlQIxgX_RTk5jOGYIm8gGXiR2qyLfi_HGzRoBIdds7xN2So2xifqrCF_aBJBq3sfKPj3A..&box_client_name=box-content-preview&box_client_version=2.62.0)
   右上方有說如果不知道要安裝哪個版本就裝推薦的版本
   
   點 **I accept this License**，我使用他預設的安裝 按下一步安裝
2. Start Command Prompt with Ruby

   安裝完後，應用程式會多個 Start Command Prompt with Ruby
   ![](https://public.boxcloud.com/api/2.0/internal_files/767667203983/versions/819052181983/representations/jpg_paged_2048x2048/content/1.jpg?access_token=1!1htqL0bloHNaBjGmy270-dIfgFi5KbOSszBXE-wYm0U-d9WdHITsB4VBPWnfO-FAAJAQOYAriWzc-M--wrFlNKaCOZoYbxKZ9gBfzDn1_QLEdPcL3Lula0GL3nsIc38kfWrlX2XLWUhnJyEgjIbgN3pWbIxRJmN9q2Bw-MdE3-LwOiEZRnuob-in0WK_w2cbyfg_QRmTG57m2aEIulNXOqgXo2rZvYloxpK4A5eWbSRIStUs3Sk_Yt1nqoa_OvlQn9a6F307iyLgQcpt4JE-TKsup2Tj_T2pr9PPkqs9jUrkiaWC8_7NlnGRKVoIyCQZ31zOW-38X1NlCjM73F2OBoDScV_q-1WLBhoYyHIacel4YkHitXjddTY21aSginR86-k8XOuQGt71HArp8sPNRUm3YtE4mTg-Kv2aYDE0kPMXQSQCVp9EvnGZLzXb8zePCMxRVun8ZFPiKlN7Zw3n9-TnyuEESGbffAQ3NGUoGZKPw76O7gl0VMUtzd5o44ywhXxN4J6kc2VYigqPQrAaUDiFOAFlC1zmsna97s32Od74QUMTGj6m4JhJ_rEkxCcXAIggKX12sA3RzGhQzZw2IHyXb7ya0zQMR7sGzYCVwR6YQG4RTT8VI_FkclREJ4uYJSOjBUAfyK4vced030zIwUa9YeigiqTz4eu1GVIWfKYKcw..&box_client_name=box-content-preview&box_client_version=2.62.0){: width="400"}


## Install jekyll
接下來可以按照 官網上 [Quick start](
) 上的順序安裝 jekyll 和 new Jekyll site 

在command 指令上輸入 安裝指令 

Install the jekyll and bundler `gems`.
```terminal
gem install jekyll bundler
```
Create a new Jekyll site at ./myblog
```terminal
jekyll new myblog
```
Change into your new directory.
```terminal
cd myblog
```
Build the site and make it available on a local server.
```terminal
bundle exec jekyll serve
```

Browse to http://localhost:4000

## [jekyll themes](http://jekyllthemes.org/)
可以使用別人已經寫好的外觀，不過在使用前還是要先看一下read。看一下使用的規則

