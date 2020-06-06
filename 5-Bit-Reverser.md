### Question 1
**How many clocks does it take for a change in DataIn to be reflected on DataOut?**
```
module BitReverser (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    ouput logic [7:0] DataOut
);

    assign DataOut[7] = DataIn[0];
    assign DataOut[6] = DataIn[1];
    assign DataOut[5] = DataIn[2];
    assign DataOut[4] = DataIn[3];
    assign DataOut[3] = DataIn[4];
    assign DataOut[2] = DataIn[5];
    assign DataOut[1] = DataIn[6];
    assign DataOut[0] = DataIn[7];
    
endmodule
```

- [x] 0
- [ ] 1
- [ ] 4
- [ ] 8


### Question 2
**How many levels of logic are there between DataIn and DataOut?**
```
module BitReverser (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    ouput logic [7:0] DataOut
);
    
    assign DataOut[7] = DataIn[0];
    assign DataOut[6] = DataIn[1];
    assign DataOut[5] = DataIn[2];
    assign DataOut[4] = DataIn[3];
    assign DataOut[3] = DataIn[4];
    assign DataOut[2] = DataIn[5];
    assign DataOut[1] = DataIn[6];
    assign DataOut[0] = DataIn[7];
    
endmodule
```

- [x] 0
- [ ] 1
- [ ] 4
- [ ] 8


### Question 3
**If we used lookup tables with 4 inputs and 1 output to implement the BitReverser module, how many lookup tables would be used?**
```
module BitReverser (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    ouput logic [7:0] DataOut
);
    
    assign DataOut[7] = DataIn[0];
    assign DataOut[6] = DataIn[1];
    assign DataOut[5] = DataIn[2];
    assign DataOut[4] = DataIn[3];
    assign DataOut[3] = DataIn[4];
    assign DataOut[2] = DataIn[5];
    assign DataOut[1] = DataIn[6];
    assign DataOut[0] = DataIn[7];
    
endmodule
```

- [x] 0
- [ ] 1
- [ ] 4
- [ ] 8


### Question 4
**How many registers does this design implement?**
```
module BitReverser (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    ouput logic [7:0] DataOut
);

    assign DataOut[7] = DataIn[0];
    assign DataOut[6] = DataIn[1];
    assign DataOut[5] = DataIn[2];
    assign DataOut[4] = DataIn[3];
    assign DataOut[3] = DataIn[4];
    assign DataOut[2] = DataIn[5];
    assign DataOut[1] = DataIn[6];
    assign DataOut[0] = DataIn[7];
    
endmodule
```

- [x] 0
- [ ] 1
- [ ] 4
- [ ] 8
