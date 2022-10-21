> **當 while 迴圈條件成立時**

**迴圈使用方法- while：while 後面括號裡面設立執行的條件，條件成立時就執行縮排內的程式。**

while迴圈在括號內設立條件判斷，只要條件成立就會重複執行，直到條件不成立為止，不同於for迴圈，while迴圈有一個很重要的觀念是「**只要條件符合，就會一直執行**」，因此適合用於「不確定會執行幾次，但只要條件符合就一直執行」的情況，**利用 number 每次控制迴圈**

```python
number=3

#number小於8重複輸出下列縮排內程式
while(number<8): 
   print(number)
   #控制迴圈執行狀況的變數 number(每次+1)
   number+=1
```

while迴圈可以搭配if條件判斷使用

while架構也有一種寫法是「**while(True):**」，意即「**條件判斷一直成立**」，True代表為真、成立，這邊需注意布林值的 **True 與 False 的開頭字母需大寫。**

**無窮迴圈**：使用 while(True) 但沒有設立「break」停著迴圈，則會無窮迴圈的情況，勿輕易嘗試無窮迴圈，電腦容易當機。

```python
number=0
while(1): #括號內不為0，則代表while(True)
   if(number==3): 
      break
   print(number)
   number+=1
```

程式中所學的知識都可以相互使用：在 if 中可以再多一層 if ；在 for 迴圈當中可以再多一層 while 迴圈；先使用 if 再包入 while 迴圈，這些都是可以的，**只要邏輯成立**，就可以使程式順利執行。

```python
math_score=90
if(math_score==100):
    number=0
    while(number<10):
        print(number+1,"獎勵雞排")
        number+=1
elif(math_score>=90):
    number=0
    while(number<3):
        print(number+1,"獎勵雞排")
        number+=1
else:
   print("無獎勵")
```

\如果數學考試考了100分，就會得到10張「獎勵雞排兌換卷」

\若數學分數介於90~100之間(不包含100分)，就會得到3張「獎勵雞排兌換卷」

\若低於90分，則「無獎勵」

```python
a=0
sum=0

#設立「while迴圈」
while(a<20): 
    if(a%2==0): #若a為偶數
        #sum加總a
        sum+=a
    #變數a做更動以控制while迴圈
    a+=1
print(sum)
```

