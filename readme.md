# 1. 實驗題目

撰寫簡易語法 pop 與 push 之觀測結果

# 2. 實驗步驟

  1. 為方便觀察，先以 mov 賦予 r0、r1、r2 數值，並撰寫 push 、 pop 指令。先以 push {r0,r1,r2} 作為實驗程式碼。
  main.s:
  
  2. 將 main.s 編譯並以 qemu 模擬。
  ![image](https://github.com/PoChunChiu/ESEmbedded_HW02/blob/master/img_folder/ESE_or.JPG)
  
  3.觀察 push 、 pop 之運作。使用push {r0,r1,r2}可以看到 sp 、pc 與 msp皆有改變。

![image](https://github.com/PoChunChiu/ESEmbedded_HW02/blob/master/img_folder/push_012.JPG)
  
  4. 以 vim 編輯 main.s，但改以 push {r2,r0,r1}作為實驗程式碼，重複步驟2。

# 3. 結果與討論

  1. pop 會將先前 push 最後置入之元素取出，置入 pop 之餘元素。
  
  2. 改變 push 之順訊由{r0,r1,r2}至{r2,r0,r1}並不影響結果，但在 make 階段會因為 register range 並非升冪造成的 warning ，並替我們修正:
  ![image](https://github.com/PoChunChiu/ESEmbedded_HW02/blob/master/img_folder/warning.JPG)


--------------------

- [ ] **If you volunteer to give the presentation next week, check this.**

--------------------

      






