from collections import Counter
#1
text = "hello world"
print("Length of string:", len(text))
#2
text = "google.com"
print("Character frequency:", dict(Counter(text)))
#3
string_both_ends = lambda s: s[:2] + s[-2:] if len(s) >= 2 else ""
print(string_both_ends("w3resource"))
print(string_both_ends("w3"))
print(string_both_ends("w"))
#4
print((lambda s: s[0]+s[1:].replace(s[0],"$"))("restart"))
#5
print((lambda a,b: b[:2]+a[2:]+" "+a[:2]+b[2:])("abc","xyz"))
#6
add_ing = lambda s: s if len(s)<3 else s+"ly" if s.endswith("ing") else s+"ing"
print(add_ing("abc"))
print(add_ing("string"))
print(add_ing("go"))
#7
def not_poor(s):
    return s[:s.find("not")]+"good"+s[s.find("poor")+4:] if (s.find("not")!=-1<s.find("poor")) else s

print(not_poor("The lyrics is not that poor!"))
print(not_poor("The lyrics is poor!"))
#8
def longest(words):
    w = max(words, key=len)
    return w, len(w)

print(longest(["PHP","Exercises","Backend"]))
#9
remove_n = lambda s,n: s[:n]+s[n+1:]
print(remove_n("Python",2))
#10
swap = lambda s: s[-1]+s[1:-1]+s[0] if len(s)>1 else s
print(swap("Python"))
#11
odd_out = lambda s: s[::2]
print(odd_out("Python"))
#12
from collections import Counter
print(Counter("the cat and the hat".split()))
#13
def convert_case(s): return s.upper(), s.lower()
print(convert_case("HelloWorld"))
