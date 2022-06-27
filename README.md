# PYTHON

###  LECTURE 01: HELLO WORLD, NUMBER & STRING IN PYTHON

#### 1. Hello world

```
print('Hello world')
print("Hello, World")
```

Assignment and equal operation

```
a = 999
b = a + 1  #  b = 1000
print(b)
```

#### 2. Standard Data Types
##### 2.1. Numerical data type

- integer 
- float
- bytes
- hex
- complex

###### Modulo
Phép chia lấy phần dư `6 % 2  # 6 chia lấy phần dư cho 2 -> 0`

###### Lũy thừa

```
a = 2
b = a**10
print(a)
print(b)
```

###### Number Conversions

```
a = 123 # integer
float(a)
```

##### 2.2. Strings

###### Convert

```
a = "123.4"
float(a)
str(123.4)
```

###### Slicing

```string[start:stop:step]``` -> return chuỗi ký tự từ gồm các ký tự từ vị trí start đến vị trí stop - 1 với bước nhảy step

###### viết tắt:
 - không khai báo start thì mặc định lấy từ đầu xâu đến stop-1
 - không khái báo stop thì mặc định lấy đến cuối xâu

###### Reverse string

`s[::-1]`

###### String methods
https://docs.python.org/3/library/stdtypes.html#string-methods

- capitalize first character: `r.capitalize()`
- uppercase: `r.upper()`
- lowercase: `r.lower()`
- swap upper and lower: `r.swapcase()`
- title: `a.title()`
- count: `r.count("z")`

###### leading and trailing characters
- str.strip()
- str.lstrip()
- str.rtrip()

###### find substring
```str.find(character, [start, stop])``` -> trả về index của ký tự cần tìm ở substring từ start -> stop - 1 

###### Check method:
- str.isalpha(): xâu có chứa ký tự alphabet hay không
- str.isdigit(): xâu có chứa ký tự là số hay không
- str.isalnum(): xâu có chứa ký tự là alphabet và số hay không

###### replace
```str.replace(old, new, max)``` -> replace old bằng new với số lần thay thế là max lần

###### Để giải quyết vấn đề, coi ký tự thoát chỉ là ký tự thì ta có 2 cách:
- Cách 1. sử dụng \\\
- Cách 2. sử dụng r trước xâu

#### 3. Input/Output

Syntax: ```input()``` -> trả về __giá trị kiểu String__ thể hiện giá trị do người dùng nhập vào

```
print("Chào bạn " + name + ", năm nay bạn " + str(age) + " tuổi.")
print("Chào bạn %s, năm nay bạn %s tuổi." % (name, age))
print("Chào bạn {}, năm nay bạn {} tuổi.".format(name, age))
print(f"Chào bạn {name}, năm nay bạn {age} tuổi.")
```