### Question 1
**For the following gates, select the correct output value F and G given inputs A=0, B=0, C=1, D=1**
![Logic1](/images/logic1.png)

- [ ] F=0, G=0
- [ ] F=0, G=1
- [ ] F=1, G=0
- [x] F=1, G=1

> *Explanation:* 
> ```**F** = (A and B) nand (C or D) = 0 nand 1 = 1``` | 
> ```**G** = (A and B) xor (C or D) = 0 xor 1 = 1```

### Question 2
**For the following gates, select the correct output value F and G given inputs A=1, B=1, C=0, D=1**
![Logic1](/images/logic1.png)

- [x] F=0, G=0
- [ ] F=0, G=1
- [ ] F=1, G=0
- [ ] F=1, G=1

> *Explanation:* 
> ```**F** = (A and B) nand (C or D) = 1 nand 1 = 0``` | 
> ```**G** = (A and B) xor (C or D) = 1 xor 1 = 0```

### Question 3
**For the following gates, select the correct output value F and G given inputs A=0, B=0, C=0, D=1**
![Logic2](/images/logic2.png)

- [ ] F=0, G=0
- [ ] F=0, G=1
- [x] F=1, G=0
- [ ] F=1, G=1

> *Explanation:* 
> ```**F** = (not(A and B)) and (C or D) = 1 and 1 = 1``` | 
> ```**G** = (A and B) xnor (C or D) = 0 xor 1 = 0```

### Question 4
**For the following gates, select the correct output value F and G given inputs A=0, B=0, C=0, D=0**
![Logic2](/images/logic2.png)

- [ ] F=0, G=0
- [x] F=0, G=1
- [ ] F=1, G=0
- [ ] F=1, G=1

> *Explanation:* 
> ```**F** = (not(A and B)) and (C or D) = 1 and 0 = 0``` | 
> ```**G** = (A and B) xnor (C or D) = 0 xor 0 = 1```

### Question 5
**For the following gates, select the correct output value F and G given inputs A=1, B=1, C=1, D=1**
![Logic3](/images/logic3.png)

- [ ] F=0, G=0
- [x] F=0, G=1
- [ ] F=1, G=0
- [ ] F=1, G=1

> *Explanation:* 
> ```**F** = (not(A and B)) and (not(C xor D)) = 0 and 1 = 0``` | 
> ```**G** = (A and B) xor (C xor D) = 1 xor 0 = 1```

### Question 6
**For the following gates, select the correct output value F and G given inputs A=0, B=0, C=0, D=0**
![Logic3](/images/logic3.png)

- [ ] F=0, G=0
- [ ] F=0, G=1
- [x] F=1, G=0
- [ ] F=1, G=1

> *Explanation:* 
> ```**F** = (not(A and B)) and (not(C xor D)) = 1 and 1 = 1``` | 
> ```**G** = (A and B) xor (C xor D) = 0 xor 0 = 0```
