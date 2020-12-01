# tugas-pertemuan-10
# labs06danlabs07
**Nama	   	: Siti Latifah** <br>
**Nim	  	  : 312010321** <br>
**Kelas	  	: TI.20.A2** <br>
**Matkul	  : Bahasa Pemrograman** <br>


# Praktikum 6
## Latihan 1
![Screenshot (56)](https://user-images.githubusercontent.com/73010098/100722150-de52c280-33f2-11eb-8fd9-ab5f6130655c.png)
## Syntax
```python
#def a(x):
#return x**2
a = (lambda x: x ** 2)
print(a(10))

#def b(x, y):
#return math.sqrt(x**2 + y**2)
b = (lambda x,y: x**2 + y**2)
print(b(4,8))

#def c(*args):
#return sum(args)/len(args)
c = (lambda *args: sum(args)/ len(args))
print(c(4))

#def d(s):
#return "".join(set(s))
d = (lambda s: "".join(set(s)))
print(d("vwxyz"))
```
## OUTPUT
![Screenshot (54)](https://user-images.githubusercontent.com/73010098/100722351-1b1eb980-33f3-11eb-892d-139d7aea24c0.png)
![Screenshot (55)](https://user-images.githubusercontent.com/73010098/100722375-2245c780-33f3-11eb-91c1-c7b6282d3d70.png)



