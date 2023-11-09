# striver_python
string=""
def pal(s):
    global string
    p = ''.join(filter(str.isalnum,s))
    p=p.lower()
    l=len(p)
    if l>=1:
        string=string+p[l-1]
        pal(p[:l-1])
    else:
        return
s="A man, a plan, a canal: Panama"
d=''.join(filter(str.isalnum,s))
d=d.lower()
pal(s)
if string==d:
    print("true")
else:
    print("false")
