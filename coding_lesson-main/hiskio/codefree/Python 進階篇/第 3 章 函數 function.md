**function 設定格式架構**

> **直接使用函式**

e.g. sum()函式

```python
score=[88,90,76]
print(sum(score))
```

**排序函式 sorted()**

由小到大排序

```python
score=[88,90,76]
print(sorted(score))
```

> **自定義函式**

```python
def 自定義函式的名稱(傳入的參數資料):
	#縮排內都是自定義函數的範圍
```

-----

利用自定義函數判斷數字「是否」為偶數

```python
def checknumpr(x):
  if(x%2==0):
    print("是偶數")
  else:
    print("不是偶數")

checknumpr(5)
```

![mcf6hclyawk9gk2.png](https://github.com/sakana-fish-owo/coding_lesson/blob/main/hiskio/codefree/Python%20%E9%80%B2%E9%9A%8E%E7%AF%87/img/mcf6hclyawk9gk2.png?raw=true)

`在python中，「和」寫and就好，「或」寫or就好，不等於寫!=`

**使用「return」回傳值撰寫自定義函式**

```python
def checknum(x):
   if(x%2==0):
      return "是偶數"
   else:
      return "不是偶數"

answer=checknum(5)
print(answer)
```

>  return 和 print的區別：
>  
> \# 在執行函數的時候***return無法打印出值***，return返回的結果只能用於給***變量賦值***。而pirnt則可以直接打印。
> 
> \# return還有一個重要特性：在函數中，凡是遇到return，這個***函數就會結束***，這裏要特別註意。針對無限循環的函數，可以使用return

-----

**全域變數與區域變數**

呼叫自定義函式時，需要注意**變數的擺放位置**，若變數擺於「自定義函式」的外面，則代表為「全域變數」；反之，則代表為「區域變數」。**將其在函式中命定「global」**

```python
a=5
def countsum(x):
    global a //將a定為全域變數
    a+=x
    return a

print("呼叫 countsum 函式之前的 a：",a)
print("呼叫 countsum 函式之後的 a：",countsum(3))
```

```python
def countsum(x):
    a=5
    a+=x
    return a
```

