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

### LECTURE 02 Boolean & Conditional Statements

#### 1. Common data types (cont.)

##### Boolean

Convert to the boolean data type using Python's bool() function. <br>
- An int, float or complex number set to **zero** -> False. <br>
- An integer, float or complex number set to **any other number, positive or negative**, -> True.<br>
- NoneType or empty value -> False <br>

##### Boolean Arithmetic

- or
- and
- not
- == (equivalent)
- != (not equivalent)

##### Membership operators

- in
- not in

##### Identity operators

- is 
- is not 

#### 2. Conditional Statements

Syntax:
```
if <câu điều kiện 1>:
    <câu lệnh thực thi nếu trường hợp điều kiện 1 được thỏa mãn>
elif <câu điều kiện 2>:
    <câu lệnh thực thi nếu trường hợp điều kiện 2 được thỏa mãn>
...
else:
    <câu lệnh thực thi ở các trường hợp còn lại>
```

##### Full case with elif, else

```
x = 8

if x < 0:
    print('negative')
elif x == 0:
    print('zero')
elif 0 < x < 10:
    print('Positive but smaller than 10')
else:
    print('Greater than 10')
```

### LECTURE 03 DATETIME & LOOP IN PYTHON

#### 1. Dates and times

```
# cach 1 : import toàn bộ module
import datetime
# để sử dụng cần gọi <tên_module>.<tên_hàm>
datetime.datetime(2022, 12, 20)

# cach 2: import toàn bộ module và gán tên (alias)
import datetime as dt
# để sử dụng cần gọi <tên_module>.<tên_hàm>
dt.datetime(2022, 12, 20)

# cach 3: import toàn bộ module
from datetime import *
# để sử dụng chỉ cần gọi <tên_hàm>
datetime(2022, 12, 20)

# cach 4: import một method nhất định từ module
from datetime import datetime, date, time, timedelta
# để sử dụng chỉ cần gọi <tên_hàm>
datetime(2022, 12, 20)
```

##### 1.1 Datetime/date and attributes

- Với các đối tượng datetime, date, time, timedelta đều có các thuộc tính để tiện quá trình extract như .year, .month, .seconds, ...

```
# lấy giá trị 'giờ' từ datetime
dt.day

# lấy thông tin từ datetime
dt.date()
```

##### 1.2 Get current datetime or date

```
# datetime.now()  # date and time
datetime.today()  # date and time
```

##### 1.3 Timedelta 
represents a duration, the difference between two dates or times.

```
time_delta = datetime.now() - datetime(2018, 9, 12, 2, 34, 12)
print(f'Hai moc thoi gian cach nhau {time_delta.days} ngay')

# 1 tuần sau là ngày bao nhiêu ?
delta = timedelta(weeks=1)
datetime.today() + delta
```

##### 1.4 Convert datetime to string and vice versa

see more at: [https://docs.python.org/3/library/datetime.html#strftime-strptime-behavior](https://docs.python.org/3/library/datetime.html#strftime-strptime-behavior)

###### 1.4.1 From string to datetime

syntax:
  ```datetime.strptime(_str_, 'format')```

###### 1.4.2 From datetime to string

```
sample_date = datetime(2018, 11, 8, 12, 18)  # YYYY/MM/DD
s_date = sample_date.strftime('%Y/%m/%d') 
print(s_date)
```

#### 2. for loops

syntax
```
for item in sequence:
    <code block>
```

##### Duyệt xâu
string trong Python chính là 1 sequence object

```
s = "Data Python"
for ch in s:  # duyệt từng ký tự trông xâu và in ký tự đó ra
    print(ch)
```

##### hàm range
syntax
```
range(start, stop, step=1)
```

```
# Print number from 0 to 9
for number in range(0, 10):
    print(number)
```

##### Hai cách để duyệt và lấy giá trị trong một string object:
 - Cách 1. loop qua chính đối tượng đó và lấy ra giá trị
 - Cách 2. loop qua giá trị chỉ mục và lấy ra giá trị dùng indexing


```
# Cách 1:
for i in s:
    print(i)

# Cách 2
for idx in range(len(s)):
    print(f'index : {idx} -> string: {s[idx]}')
```

#### 3. while loops
A while loop specifies a condition and a block of code that is to be executed *until the condition evaluates to False* or the loop is explicitly ended with *break*.<br>
syntax:
```
while <condition>:
    <codes>
```

```
# print number from 0 to 9
# print number (from 0) until the condition is False (greater than or equal to 10)
count = 0
while count < 10:  # while-condition, if True then execute code in block, else exit while-block
    print(count)
    count = count + 1
```

##### 3.1 break and continue statements

###### 3.1.1 continue

The break statement terminates the loop containing it. Control of the program flows to the statement immediately after the body of the loop.

If the break statement is inside a nested loop (loop inside another loop), the break statement will terminate the innermost loop.

```
for letter in 'Python':
    if letter == 'h':
        break  # exit loop func when hit h character
    print('Current letter :', letter)
```

###### 3.1.2 continue

The continue statement is used to skip the rest of the code inside a loop for the current iteration only.<br>Loop does not terminate but continues on with the next iteration.

```
for letter in 'Python':
    if letter == 'h':
        continue  # skip print for h character
    print('Current letter:', letter)
```

