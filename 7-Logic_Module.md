### Question 1
**How many clocks does it take for a change in DataIn to be reflected on DataOut ?**
```
module LogicModule (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    output logic [7:0] DataOut
);

    always @(Clk) begin
        DataOut[7] <= DataIn[0] or DataIn[1];
        DataOut[6] <= DataIn[1] or DataIn[2];
        DataOut[5] <= DataIn[2] or DataIn[3];
        DataOut[4] <= DataIn[3] or DataIn[4];
        DataOut[3] <= DataIn[4] or DataIn[5];
        DataOut[2] <= DataIn[5] or DataIn[6];
        DataOut[1] <= DataIn[6] or DataIn[7];
        DataOut[0] <= DataIn[7] or DataIn[0];
    end

endmodule
```

- [ ] 0
- [x] 1
- [ ] 4
- [ ] 8


### Question 2
**How many levels of logic are there between DataIn and DataOut ?**
```
module LogicModule (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    output logic [7:0] DataOut
);

    always @(Clk) begin
        DataOut[7] <= DataIn[0] or DataIn[1];
        DataOut[6] <= DataIn[1] or DataIn[2];
        DataOut[5] <= DataIn[2] or DataIn[3];
        DataOut[4] <= DataIn[3] or DataIn[4];
        DataOut[3] <= DataIn[4] or DataIn[5];
        DataOut[2] <= DataIn[5] or DataIn[6];
        DataOut[1] <= DataIn[6] or DataIn[7];
        DataOut[0] <= DataIn[7] or DataIn[0];
    end

endmodule
```

- [ ] 0
- [x] 1
- [ ] 2
- [ ] 4


### Question 3
**If we used lookup tables with 4 inputs and 1 output to implement the LogicModule module, how many lookup tables would be used?**
```
module LogicModule (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    output logic [7:0] DataOut
);

    always @(Clk) begin
        DataOut[7] <= DataIn[0] or DataIn[1];
        DataOut[6] <= DataIn[1] or DataIn[2];
        DataOut[5] <= DataIn[2] or DataIn[3];
        DataOut[4] <= DataIn[3] or DataIn[4];
        DataOut[3] <= DataIn[4] or DataIn[5];
        DataOut[2] <= DataIn[5] or DataIn[6];
        DataOut[1] <= DataIn[6] or DataIn[7];
        DataOut[0] <= DataIn[7] or DataIn[0];
    end

endmodule
```

- [ ] 0
- [ ] 1
- [ ] 4
- [x] 8


### Question 4
**How many registers does this design implement?**
```
module LogicModule (
    input logic Clk,
    input logic Rst,
    input logic [7:0] DataIn,
    output logic [7:0] DataOut
);

    always @(Clk) begin
        DataOut[7] <= DataIn[0] or DataIn[1];
        DataOut[6] <= DataIn[1] or DataIn[2];
        DataOut[5] <= DataIn[2] or DataIn[3];
        DataOut[4] <= DataIn[3] or DataIn[4];
        DataOut[3] <= DataIn[4] or DataIn[5];
        DataOut[2] <= DataIn[5] or DataIn[6];
        DataOut[1] <= DataIn[6] or DataIn[7];
        DataOut[0] <= DataIn[7] or DataIn[0];
    end

endmodule
```

- [ ] 0
- [ ] 1
- [ ] 4
- [x] 8
