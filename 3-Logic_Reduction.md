### Question 1
**Defining a gate as a 2 input function, what is the minimum number of gates needed to implement the following boolean equation?**
```
((A xor B) and C) or ((A xor B) and not C)
```
- [ ] 0
- [x] 1
- [ ] 2
- [ ] 5
- [ ] 6

> *Explanation:*
> ```((A xor B) and C) or ((A xor B) and not C) = (X and C) or (X and not(C)) =[distributive]= X and (C or not(C)) =[complement]= X and 1 = X = A xor B```


### Question 2
**Defining a gate as a 2 input function, what is the minimum number of gates needed to implement the following boolean equation?**
```
((A or B) and C) and (A and not C)
```
- [x] 0
- [ ] 1
- [ ] 2
- [ ] 4
- [ ] 5

> *Explanation:*
> ```((A or B) and C) and (A and not C) =[distributive]= ((A and C) or (B and C)) and (A and not(C)) =[distributive]= (A and not(C) and A and C) or (A and not(C) and B and C) =[theorem]= 0 or 0 =[axiom]= 0```

### Question 3
**Defining a gate as a 2 input function, what is the minimum number of gates needed to implement the following boolean equation?**
```
(A xor B) and C
```
- [ ] 0
- [ ] 1
- [x] 2
- [ ] 3

> *Explanation:* It cannot be achieved any more minimization to this boolean function.

### Question 4
**Defining a gate as a 2 input function, what is the minimum number of gates needed to implement the following boolean equation?**
```
(A and B and C) or ((A or B) and C)
```
- [ ] 0
- [x] 2
- [ ] 3
- [ ] 4
- [ ] 5

> *Explanation:* (A and B and C) or ((A or B) and C) =[distributive]= (A and B and C) + ((A and C) or (B and C)) =[associative]= ((A and B and C) or (A and C)) or (B and C) =[absorption]= (A and C) or (B and C) =[distibutive-reverse order]= C and (A or B)
