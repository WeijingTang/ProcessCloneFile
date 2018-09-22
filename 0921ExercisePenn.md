

```python
#f = open("/Users/macbookair/Downloads/clones.tsv","r") 
f = open("clones.tsv","r")
def clones_mostoccin_samples(f):
	line = f.readlines()[1:]
	d = {}
	for l in line:
		if l.split()[0] not in d.keys():
			d[str(l.split()[0])] = 1
		else:
			d[str(l.split()[0])] = d[str(l.split()[0])] + 1
	list = sorted(d,key=d.get)
	location = list[len(list)-1]
	return location

def clone_highest_total_cnt(f):
	line = f.readlines()[1:]
	d = {}
	for l in line:
		if l.split()[0] not in d.keys():
			d[str(l.split()[0])] = int(l.split()[2])
		else:
			d[str(l.split()[0])] = d[str(l.split()[0])] + int(l.split()[2])
	list = sorted(d,key=d.get)
	clone = list[len(list)-1]
	return clone

def cdr3_occ_multi_clone(f):
	line = f.readlines()[1:]
	d = {}
	for l in line:
		if l.split()[3] not in d.keys():
			a = []
			a.append(str(l.split()[0]))
			d[l.split()[3]] = a   
		else:
			d[l.split()[3]].append(str(l.split()[0])) 
	list = {}
	for k,v in d.items():
		if len(v) > 1:
			list.update({k : len(v)})
	return list

#clone_highest_total_cnt(f)
#clones_mostoccin_samples(f)
#cdr3_occ_multi_clone(f)
```
