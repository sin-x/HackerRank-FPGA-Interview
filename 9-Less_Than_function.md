### Question 1

**Implement a lessThan function with the following signature:**

```function bool lessThan(Date d1, Date d2);```

**Assume that Date is a struct/record with integer members Day , Month , and Year . Your implementation should return true if d1 represents an earlier date than d2 and false otherwise.**

```
-- code in VHDL

function lessThan (d1, d2 : date) return boolean is

    variable year_gr, year_eq, month_gr, month_eq, day_gr, result : boolean;
    
begin
    
    year_gr := d2.year > d1.year;
    year_eq := d2.year = d1.year;
    month_gr := d2.month > d1.month;
    month_eq := d2.month = d1.month;
    day_gr := d2.day > d1.day;

    result := year_gr OR (not(year_gr) AND year_eq AND month_gr) OR (not(year_gr) AND year_eq AND not(month_gr) AND month_eq AND day_gr);
    return result;
    
end lessThan;
```
