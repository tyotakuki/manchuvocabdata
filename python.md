# Manju gisun -i Python -i Temgetu Jorin
Python oci emu hacin -i necinkaran siden [^1] on weilere [^2] bodotun gisun Windows, OS X embici Ubuntu -i Terminal -i selgiyen jombukv [^3] -i dorgide
```
>>> python3.11
```
seme tantafi Python -i tungselekv [^4] be dekdebuci ombi. Python -i kode -i geren jurgan -i teisu tab ibeden [^5] baibumbi. Tab ibeden geren cike -i jergi ilhi jai ini kvwaran be tuwabumbi:
```python
if A:
    B
else:
    C
    while D:
        E
```

## Data jai Kvbulikv
Python -i kvbulikv -i gebu fejergi -i geren baibushvn de acanaci acambi:
- emu gargata hergen embici fejergi jijun deri deribuci acambi.
- ton deri deriburakv oci acambi.
- damu alfangga[^6] embici tongga hergen jai fejergi jijun baktambi.
- kvbulikv -i gebu oci amba-buya serecuke [^7].

Emu kvbulikv de uttu hvda tomilambi:
```python
x = 1
y = "orange"
z = 3.14
```
Geli udu kvbulikv de uttu enculeme hvda tomilaci ombi, "alhvdan teisulere/teisulen"[^8] sembi.
```python
x, y, z = 1, "orange", 3.14
```
Geli udu kvbulikv de emu gesengge hvda -i tomilaci ombi.
```python
x = y = z = "orange"
```
Geli yaya emu isabun be ebubufi udu kvbulikv -i hvda gaimbi.
```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
```
Geli emu fejergi jijun -i nergin -i kvbulikv [^9] be toktombi.
```python
x, y, _ = [1, 2, 3]
```
`print` sere fakjin -i kvbulikv -i hvda be tucibufi tantabuci ombi.
```python
x = "abc"
print(x)
```

Fafulabuhangge ci tulgiyen eiten kvbulikv oci tesungge kvbulikv [^10]

```global``` sere oyonggo gibsun -i yaya emu kvbulikv be gubcingga kvbulikv [^11] obumbi.
- Emu fakjin -i dorgi fafulabuha kvbulikv oci gubcingga ba -i hartungga.
- Emu fakjin -i dorgi ini tulergide fafulabuha toktobuha kvbulikv be baitalaci ombime, fakjin -i dorgi bade kvbulibuci ojorakv. Tuttu bime, aika ere fakjin -i dorgi ```global``` sere oyonggo gibsun -i fafulafi teni fakjin -i dorgi bade hvda kvbulibuci ombi.

Duibuleci,
```python
def myfunc():
  global x
  x = "fantastic"
myfunc()
print("Python is " + x)
```
geli
```python
x = "awesome"
def myfunc():
  global x
  x = "fantastic"
myfunc()
print("Python is " + x)
```

## Data -i Duwali
Python de udu hacin -i data duwali bi:
- hergengge: `str`
- tongga: `int`, `float`, `complex`
- sirengge: `list`, `tuple`, `range`
- fakjilangga: `dict`
- isabungga: `set`, `frozenset`
- boolonggo: `bool`
- juwengge: `bytes`, `bytearray`, `memoryview`
- akvngga: `NoneType`
Yaya emu kvbulikv -i duwali be `type()` sere fakjin -i gaici ombi.
```python
x = 5
print(type(x))
```
Geli ememu duwali -i gebu be fakjin seme baitalaci wembumbi.
```python
x = int(20.5)
print(x)
# 20
```
`int` oci gulhun ton -i duwali.
`float` oci neore tongki ton [^12] -i duwali.
`complex` oci largin ton -i duwali, tebici
```python
x = 1+2j
```
Yaya hacin -i tongga duwali deri `str()` -i ini hergen derei [^13] hergen futa/ulcin [^14] de wembumbi.

Emu `string` oci hergen ulcin -i duwali inu. Juwe dubede emursu embici jursu yarure koki [^15] sindambi. Tebici `x = 'string'` embici `y="string"`.

Labdu meyen -i hergen ulcin bici ilan jursu koki deribun de geli wajin de sindambi.
```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```

Hergen ulcin -i dorgi -i geren feten be `[]` (durbejen taka) -i gaici ombi. Tebici `x = 'abc'` bici `'a'` be `x[0]` seme gaici ombi. Eiten hergen ulcin -i fejergi kemun [^16] urunakv 0 ci deribumbi. Lala feten be `x[-1]` seme, amasi toloro juweci feten be `x[-2]` seme gaimbi.

Geli `[]` -i yaya emu hergen ulcin be farsilaci ombi. Tebici `x[2:6]` -i ulcin `x` -i juweci feten deri (baktamburakv -i) ningguci ningge isitala gaimbi, uheri `x[2]` deri `x[5]` (aika bici) isitala baktambumbi. `x[:5]` deribun deri bime `x[5:]` wajin de isitala farsilambi.

Juwe embici elei ulcin be `+` -i sirabufi ishunde adaci ombi. Tebici `x = "hello"` jai `y = "world"` bifi `x + y` -i `"helloworld"` gaimbi.

Yaya emu hergen ulcin oci dabtacuka [^17]. `for` sere forgoxon -i yaya emu hergen ulcin -i dele forgoxoci ombi.
```python
for x in "banana":
  print(x)
```
`in` sere oyonggo gibsun -i yaya emu hergen temgetu be emu hergen ulcin -i dorgide bisire bisirakv seme duilembi. Geli sirke fejergi hergen ulcin -i bisire bisirakv seme duileci ombi.
```python
txt = "The best things in life are free!"
print("free" in txt)
```
Akvci `not in` be baitalaci ombi.

Aika alfangga tongga hergen ci tulgiyen ASCII hergen be dosibuki seci, ukara hergen [^18] baibumbi. Tebici
| Hergen | Ukara Hergen |
|-----|-----|
|emursu koko ' | `\'`|
| jursu koki " |  `\"` |
| ice meyen | `\n`|
| sejen bederere | `\r`|
| tab | `\t`|
| siden marire [^19] | `\b` |
| ice afaha | `\f` |
| jakvngga hvda | `\ooo` |
| niolhvngga hvda | `\xhh` |

## Boolonggo Kvbulikv
Boolonggo kvbulikv damu juwe 0/1 embici `True/False` (meimeni "uru/waka" -i gvnin) hvda gaici acambi. Tebici, `==`, `>` jai `>=`, `<` jai `<=` bisire iletubun gemu boolonggo kvbulikv bi. 

Yaya emu boolonggo akv kvbulikv deri `bool()` -i emu boolonggo kvbulikv de wembuci ombi. An -i ucuri amba ubu -i hvda gemu `True` banjibumbime, `None`, `0`, `[]`, `""`, `()`, `{}` geli fejergi -i hacin -i hacinduwali [^20] deri gemu `False` be bahambi.
```python
class myclass():
  def __len__(self):
    return 0
```

## (Tolocin -i) Icihiyakv [^21]
Yaya hacin -i tolocin -i icihiyakv gemu Python -i icihiyakv. Tebici,
| Icihiyakv | Icihiyara arga |
|-----|-----|
| `+` | nonggire arga|
| `-` | ekiyembure arga|
| `*` | kamcire arga|
| `/` | faksalara arga|
| `%` | modulara [^22] arga|
| `**` | hvsun |
| `//` | ferengge faksalarangga|

Juwengge tolocingga icihiyara arga bi.

| Icihiyakv | Icihiyara arga |
|-----|-----|
| `&` | bit -i songkoi JAI|
| `\|` | bit -i songkoi EMBICI|
| `^` | bit -i songkoi WAKA|
| `~` | geren bit be fudarame obure|
| `>>` | jebesi anara [^23] |
| `<<` | hashvsi anara|

Geli gvwa udu hacin -i icihiyakv bi.

### Tomilara Icihiyakv
Python de tolocin -i icihiyakv baitalafi tesu kvbulikv be kvbulibure icihiyakv bi.
| Icihiyakv | Icihiyara arga |
|-----|-----|
| `+=` | nonggifi hvda tomilara|
| `-=` | ekiyembufi hvda tomilara|
| `*=` | kamcifi hvda tomilara|
| `/=` | faksalafi hvda tomilara|
| `%=` | modulafi hvda tomilara|
| `**=` | hvsun gamafi hvda tomilara |
| `//=` | ferengge faksalafi hvda tomilara|
| `&=` | bit -i songkoi JAI gaifi hvda tomilara|
| `\|=` | bit -i songkoi EMBICI gaifi hvda tomilara|
| `^=` | bit -i songkoi WAKA gaifi hvda tomilara|
| `>>=` | jebesi anafi hvda tomilara|
| `<<=` | hashvsi anafi hvda tomilara|
Geli gvwa udu hacin -i icihiyakv bi.

### Duibulere Icihiyakv
| Icihiyakv | Icihiyara arga |
|-----|-----|
| `==` | ishunde teherere|
| `!=` | ishunde tehererakv|
| `>` | amba|
| `<` | buya|
| `>=` | amba embici ishunde teherembi|
| `<=` | buya embici ishunde teherembi|

### Logikangga Icihiyakv
| Icihiyakv | Icihiyara arga |
|-----|-----|
| `and` | logikangga JAI|
| `or` | logikangga EMBICI|
| `not` | logikangga WAKA|
### Ubu Sibiyangga Icihiyakv
| Icihiyakv | Icihiyara arga |
|-----|-----|
| `is` | gesengge bakcilakv [^24] |
| `is not` | gesengge bakcilakv |

### Gaksishvn [^25] Icihiyakv
| Icihiyakv | Icihiyara arga |
|-----|-----|
| `in` | -i emu gaksi |
| `not in` | -i emu gaksi waka |

## Isamjangga Bakcilakv
Python de duin hacin -i isamjangga bakcilakv bi.
- `list`: Manju gisun de futa, faidan, meyen sembi.
- `tuple`: Manju gisun de ursu [^26] sembi.
- `set`: Manju gisun de isabun sembi.
- `dict`: Manju gisun de buleku sembi.

### Meyen
Meyen serengge, geren (ishunde encu duwali bisire) kvbulicuke [^27] jaka be ilhi bisire ome isamjarangge.
```python
mylist = ["abc", 34, True, 40, "male"]
```

Meyen -i dorgi -i geren gaksi be hergen ulcin -i gesengge muru be dahame `[]` sere icihiyakv -i gaici ombi. Meyen de fejergi -i udu arga [^28] bi:
- ememu oron -i hvda be kvbulirengge: `x[2] = 'a'` be dahame `x` -i juweci oron de `'a'` -i tomilambi.
- dosimburengge: `x.insert(2, 'a')` be dahame `x` -i juweci oron de `'a'` be dosimbumbi.
- uncehen de nonggirengge: `x.append('a')` be dahame `x` -i uncehen de emu `'a'` nonggimbi.
- adarangge: `x.extend(y)` be dahame, juwe meyen embici dabtacuka be ishunde adame holbobumbi. Geli `x + y` be baitalaci ombi.
- jibsiburengge: aika `x` inu `[1,2,3]` oci, `x ** 3` sere cike `[1,2,3,1,2,3,1,2,3]` bumbi.
- geteremburengge: `del x[2]` embici `x.pop(2)` be dahame, 2-ci oron -i gaksi be geterembumbi. Amala ningge geli tesu meyen -i 2-ci oron -i hvda be isibumbi.
- golmin: `len()` be baitalame emu meyen -i golmin be gaici ombi.
- oron: `x = [1,2,3,2]` bifi, `x.index(2)` sere cike `2` -i xuwe neden -i jorire oron `1` bumbi. Terei amala jai tucike `2` be melebuhe.
- toloronggo: `x = [1,4,3,4]` bifi, `x.count(4)` sere cike `2` -i uheri ton be tolofi, `4` bumbi.

**Oyonggon** Eiten meyen be aika fakjin de adaha kvbulikv [^29] seme buci, fakjin -i beyei dorgide kvbulibuci tesu meyen geli teisuleme dahafi kvbulimbi. Tebici,
```python
def myfun(z):
    z += [len(z)]

x = [1,2,3]
myfun(x)
print(x)
# [1,2,3,3]
myfun(x)
print(x)
# [1,2,3,3,4]
```
Aika `x` -i hvda be fakjin -i dorgide kvbuliburakv oki seci, `myfun(x[:])` be baitalaci acambi.

Tuttu bime, aika `x` damu emu tongga kvbulikv bici, ini hvda be uttu kvbulibuci ojorakv.

### Ursu
Ursu serengge, geren ishunde gesengge duwali bisire kvbulicuke akv jaka be ilhi bisire ome isamjarangge.
```python
mytuple = ("abc", 34, True, 40, "male")
```
embici
```python
mylist = ["abc", 34, True, 40, "male"]
mytuple = tuple(mylist)
```
Usiha -i temgetu `*` -i emu ursu be ebubuci ombi. An -i ucuri juwe hacin -i baitalabun bi:
- emu fakjin -i adaha kvbulikv [^27] seme baitalabuci ombi.
```python
mytuple = ("abc", 34, True, 40, "male")
myfun(*mytuple)
```
jai
```
myfun("abc", 34, True, 40, "male")
```
de ishunde teherxembi.
- emu ursu -i dorgi alhvdan teisulembi.
```python
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")
(green, yellow, *red) = fruits
print(red)
# ("cherry", "strawberry", "raspberry")
```
```python
fruits = ("apple", "mango", "papaya", "pineapple", "cherry")
(green, *tropic, red) = fruits
print(tropic)
# ("mango", "papaya", "pineapple")
```

### Isabun
Emu isabun serengge, udu ishunde adali akv jaka be ilhi akv, dahirakv -i isaburengge.
```python
thisset = {"apple", "banana", "cherry", "apple"}
print(thisset)
# {'apple', 'cherry', 'banana'}
myset = {"abc", 34, True, 40, "male"}
# {"abc", 34, True, 40, "male"}
``` 
Meyen jai ursu de adali akv, gvwa arga sa be baitalame gaksi be nonggire ekiyembuci acambi.
- `.add()` -i emteli gaksi be nonggime `.update(ITERABLE)` -i udu gaksi be nonggimbi.
- `.remove()` -i emteli gaksi be ekiyembumbi. Aika tere gaksi ere isabun -i dorgide bisirakv oci, emu taxan banjibumbi.
- `.discard()` -i emteli gaksi be ekiyembumbi. Aika tere gaksi ere isabun -i dorgide bisirakv ocibe taxan banjiburakv.
- `.pop()` geli emteli gaksi be ekiyembumbi, meyen jai ursu -i adali tere ekiyembuhe gaksi be isibumbi.
- `a.union(b)` be dahame juwe isabun `a` jai `b` be ishunde acabufi, acabuha isabun be isibumbi.
- `a.intersect(b)` be dahame juwe isabun `a` jai `b` be ishunde hiyahabufi, hiyahabuha isabun be isibumbi.


### Buleku
Python -i emu buleku serengge, yaya emu _anakv_ [^30] de emu hvda tomilarangge. `.keys()` jai `.values()` be baitalame emu buleku -i anakv -i isabun jai hvda -i meyen gaici ombi. Buleku oci kvbulicuke, ilhi bisire, inde dabkvrilaha gaksi [^31] akv.

Buleku -i eiten anakv _haxilacuke_ [^32] oci acambime, kvbulicuke bakcilakv waka oci acambi. Tuttu ofi, hergen ulcin, ursu, ton sere hacin -i bakcilakv ombi seme, meyen -i hacin -i bakcilakv ojorakv. Geli aika emu _haxi fakjin_ be baitalame hvda bodoci, meyen -i adalingga hacin -i bakcilakv deri haxi hvda bodoci ojorakv. Emu buleku be geli `haxi iletun` sembi.

`.items()` baitalafi emu buleku -i dorgi -i eiten hacin be baktambure dabtacuka be isibumbi. Duibuleci
```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
car.items()
# dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])
```
Aika emu anakv de fakjingga hvda kvbulibuki seci, embici fio seme `car["year"] = 2000` seme embici `car.update({"year": 2020})` seme arambi. Aika ememu nonggibuki sere anakv daci buleku -i dorgide akv seci, `.update()` baitalame hvda hacin nonggici ombi sehei `[]` baitalame nonggici ojorakv. `del`, `.pop(KEY)`, `.popitem()` seme hacin ekiyembuci ombi. `.copy()` seme emu buleku deri ini ikiri [^33] gaimbi.

### Banjibukv, Meyen de Hafumbi
`for` sere forgoxon -i emu meyen/dabtacuka -i dele forgoxoro anggala, Python de geli banjibukv/meyen hafurangge sere agvra baitalaci ombi. Duibuleci,
```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
print(newlist)
# ['apple', 'banana', 'mango']
```
Eitereci, emu banjibukv enteke cike kooli [^34] be dahambi:
```python
ICE_MEYEN = [ILETUBUN for HACIN in DABTACUKA if HACISU == True]
```
Geli duibuleci,
```python
newlist = [x.upper() for x in fruits]
print(newlist)
# ['APPLE', 'BANANA', 'CHERRY', 'KIWI', 'MANGO']
```
Banjibukv -i dorgide geli `else` baitalaci ombi.
```python
newlist = [x if x != "banana" else "orange" for x in fruits]
print(newlist)
# ['apple', 'orange', 'cherry', 'kiwi', 'mango']
```

## Eyen Kadalambi [^35]
Python de eyen kadalara oci umesi ja.
### Hacisu -i Songkoi Garganambi
Python de
```python
if HACISU_1:
    GAMAKI_SERE_CIKE 1
elif HACISU_2:
    GAMAKI_SERE_CIKE 2
elif HACISU_3:
    GAMAKI_SERE_CIKE 3
else:
    GAMAKI_SERE_CIKE 4
```
sefi, manju gisun de
```
aika HACISU_1 bici:
    GAMAKI_SERE_CIKE_1
akvci aika HACISU_2 bici:
    GAMAKI_SERE_CIKE_2
akvci aika HACISU_3 bici:
    GAMAKI_SERE_CIKE_3
akvci:
    GAMAKI_SERE_CIKE_4
```
sere gvnin.
### Forgoxon
```python
while HACISU:
    GAMAKI_SERE_CIKE
```
sefi, manju gisun de
```
damu HACISU bici akv de isitala:
    GAMAKI_SERE_CIKE be gama
```
sere gvnin.
Geli `for` forgoxon bi:
```python
for GAKSI in DABTACUKA:
    GAMAKI_SERE_CIKE
```
sefi, manju gisun de
```
GAKSI be DABTACUKA -i dorgi forgoxome:
    GAMAKI_SERE_CIKE be gama
```
Aika forgoxon -i emu mudan deri tuciki, ishun mudan dosiki seci, `continue` be baitalaci ombi.

An -i ucuri, emu cohotoi hacin -i dabtacuka `range()` be `for` forgoxon de baitalambi. Eitereci,
```python
range(DERIBUN, WAJIN[, OKSON])
```
bifi, 
```python
[DERIBUN, DERIBUN + OKSON, DERIBUN + 2 * OKSON ... DERIBUN + K * OKSON]
```
sere meyen, (`DERIBUN + K * OKSON < WAJIN`) sere hacisu de acanarangge. Tebici,
```python
for x in range(1,6):
    print(x, end = '+')
# 1+2+3+4+5+
```
```python
for x in range(1,6,2):
    print(x, end = '+')
# 1+3+5+
```

## Fakjin
Python de fakjin be uttu seme toktobu:
```python
def MINI_FAKJIN(ILETU_ADAHA_KVBULIKV [^36], *args, **kwargs):
    GAMAKI_SERE_CIKE
    return ISIBUKI_SERE_HVDA
```

Duibuleci,
iletu -i adaha kvbulikv be fakjin -i dorgi buci:
```python
def my_function(fname, lname):
  print(fname + " " + lname)

my_function("Emil", "Refsnes")
# Emil Refsnes
```
adaha kvbulikv be fakjin -i dorgi ursu/meyen seme buci:
```python
def my_function(*kids):
  print("The youngest child is " + kids[2])

my_function("Emil", "Tobias", "Linus")
```
oyonggo gibsun -i adaha kvbulikv be fakjin -i dorgi buleku seme buci:
```python
def my_function(**kid):
  print("His last name is " + kid["lname"])

my_function(fname = "Tobias", lname = "Refsnes")
```
Aika doigon -i sonjoho hvda be buci, 
```python
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("India")
# I am from India
my_function()
# I am from Norway
```
Aika ai cike fakjin -i dorgi gamaki serakv bihede, `pass` sere oyonggo gibsun baitalambi.
```python
def do_nothing():
    pass
```

Aika labdu hvda be isibuki seci, uttu seme araci acambi.
```python
def myfun(x):
    return x+1, x+2

x,y = myfun(2)
print(x)
# 3
print(y)
# 4
a = myfun(2)
print(a)
# (3, 4)
```
Tere nashvn de, isibuha hvda yargiyan -i emu ursu inu.

Geli emu justan dorgi [^37] -i lamda iletubun [^38] be toktobuci ombi.
```python
x = lambda a : a + 10
print(x(5))
# 15
```
```python
x = lambda a, b : a * b
print(x(5, 6))
# 30
```
Lamda iletubun be geli fakjin -i isibuha hvda seme obuci ombi.
```python
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)

print(mydoubler(11))
# 22
```

### Fakjin Marindambi [^39]
Emu fakjin -i dorgi ini beyebe fideci, tere fakjin be marindame fidehe sembi. Duibuleci,
```python
def fib(n):
    if n < 2:
        return n
    return fib(n-1) + fib(n-2)

# [fib(n) for n in range(16)]
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610]
```


## Hacinduwali
Hacinduwali serengge, yargiyan jalan jecen -i jakasu -i gvnijalarangge inu. Hacinduwali -i dorgi, `__init__()` sere arga be geren gaksi fukjincilambi [^40]. Emu hacinduwali deri, `__init__()` be dahame ice bakcilakv jai ini yaya emu gaksi be yargiyalaci ombi. `self` sere adaha kvbulikv emu bakcilakv -i beyebe jorimbi.
```python
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)

print(p1.name)
# John
print(p1.age)
# 36
p2 = Person("John", 36)
p2.myfunc()
# Hello my name is John
```
Hacinduwali be sirabuci ombi.
```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname
  def printname(self):
    print(self.firstname, self.lastname)

x = Person("John", "Doe")
x.printname()
# John Doe

class Student(Person):
  def __init__(self, fname, lname, year):
    super().__init__(fname, lname)
    self.graduationyear = 2019

x = Student("Mike", "Olsen", 2019)
x.__dict__
# {'firstname': 'Mike', 'lastname': 'Olsen', 'graduationyear': 2019}
```
`__dict__` sere gaksi ere bakcilakv -i geren gaksi be isibumbi.

### Dabtakv [^41]
Emu dabtakv serengge, `__iter__` jai `__next__` sere juwe arga be yargiyalaha bakcilakv. Duibuleci
```python
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self
  def __next__(self):
    x = self.a
    self.a += 1
    return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))
# 1
print(next(myiter))
# 2
print(next(myiter))
# 3
print(next(myiter))
# 4
print(next(myiter))
# 5
```
Aika dabtarangga be nakaki seci, `raise StopIteration` sere taxan be jodoci acambi.
```python
class MyNumbers:
    def __iter__(self):
        self.a = 1
        return self
  def __next__(self):
    if self.a <= 20:
        x = self.a
        self.a += 1
        return x
    else:
        raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
    print(x, end = " ")
#   1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 
```

## Fakjingga On Weilembi [^42]
### Meyen Kadalambi
Meyen -i hafurangga -i emu adali, isabun, ursu, geli buleku be uttu seme weileci ombi.
```python
{x ** 2 for x in range(1,10)}
# {64, 1, 4, 36, 9, 16, 49, 81, 25}
```
```python
{(k, v) : k + v for k in range(4) for v in range(4)}
# {(0, 0): 0, (0, 1): 1, (0, 2): 2, (0, 3): 3, (1, 0): 1, (1, 1): 2, (1, 2): 3, (1, 3): 4, (2, 0): 2, (2, 1): 3, (2, 2): 4, (2, 3): 5, (3, 0): 3, (3, 1): 4, (3, 2): 5, (3, 3): 6}
```

`all(BAKCILAKV)` aika eiten gaksi yooni `True` bici `True` seme isibumbi
```python
all([1,2,3,0])
# False
all([1,2,3])
# True
all([])
# True
```
`any(BAKCILAKV)` aika xuwe komso sehede emu gaksi `True` bici `True` seme isibumbi
```python
any([1,2,3,0])
# True
any([0])
# False
any([])
# False
```

`zip(MEYEN_1, MEYEN_2)` juwe meyen -i teisu oron -i gaksi be isabume meyen arambi.
```python
list(zip([1,2],[3]))
# [(1, 3)]

list(zip([1,2]))
# [(1,), (2,)]

list(zip([1,2],[3,4],[5,6]))
# [(1, 3, 5), (2, 4, 6)]
```

`min()`, `max()`, `sum()` sere fakjin emu meyen -i xuwe buya, xuwe amba, xoxon be meimeni bumbi.
`.sort()` emu meyen be jergilembime, `sorted(MEYEN)` emu meyen -i jergilehe meyen be isibumbi.

`map(FAKJIN, MEYEN)` sere fakjin emu fakjin -i emu meyen -i dele anan anan -i tomilambi.
```python
list(map(lambda v:v+1,[1,3,5,10]))
# [2, 4, 6, 11]
```

Module `functools` -i dorgi -i `reduce(FAKJIN, MEYEN)` sere fakjin uttu seme emu meyen -i dele arambi:
```python
#((((1+2)+3)+4)+5) be bodombi
import functools
functools.reduce(lambda x,y : x + y,[1,2,3,4,5]) 
# 15
```


[^1]: cross-platform
[^2]: programming
[^3]: command prompt
[^4]: interpreter
[^5]: indentation 
[^6]: alphabet
[^7]: case-sensitive
[^8]: pattern-matching
[^9]: temporary variable
[^10]: local = tesungge
[^11]: global variable
[^12]: float point number
[^13]: literal
[^14]: string
[^15]: single or double quote
[^16]: subscript
[^17]: iterable
[^18]: escape characters
[^19]: backspace
[^20]: class
[^21]: operator
[^22]: modulus
[^23]: shift left or right
[^24]: object
[^25]: membership
[^26]: tuple
[^27]: mutable
[^28]: method
[^29]: parameter, argument
[^30]: key
[^31]: duplicated
[^32]: hashable
[^33]: copy
[^34]: syntax
[^35]: control-flow
[^36]: explicit arguments
[^37]: inline
[^38]: lambda expression
[^39]: recursion
[^40]: initialize
[^41]: iterator
[^42]: functional programming
