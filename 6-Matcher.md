### Question 1
**What type of reset does the following code use?**
```
module Matcher (
    input logic Clk,
    input logic Rst,
    input logic DataIn,
    output logic Error,
    output logic Found
);

    logic [8:0] cnt;
    logic [2:0] dly;

    always @(posedge clk) begin
        if (Rst) begin
            dly <= 0;
            cnt <= 0;
            Error <= 0;
            Found <= 0;
        end else begin
            dly[0] <= DataIn;
            dly[1] <= dly[0];
            dly[2] <= dly[1];
            cnt <= cnt + 1;
            if (cnt == 128) begin
                Error <= 1;
            end else begin
                Error <= 0;
            end
            if (dly == 3'b101) begin
                Found <= 1;
            end else begin
                Found <= 0;
            end
        end
    end
    
endmodule
```

- [x] synchronous
- [ ] asynchronous

> *Explanation:* Signal reset [if (Rst) begin] is under the clock [always @(posedge clk) begin].

### Question 2
**How many registers does this design use?**
```
module Matcher (
    input logic Clk,
    input logic Rst,
    input logic DataIn,
    output logic Error,
    output logic Found
);

    logic [8:0] cnt;
    logic [2:0] dly;

    always @(posedge clk) begin
        if (Rst) begin
            dly <= 0;
            cnt <= 0;
            Error <= 0;
            Found <= 0;
        end else begin
            dly[0] <= DataIn;
            dly[1] <= dly[0];
            dly[2] <= dly[1];
            cnt <= cnt + 1;
            if (cnt == 128) begin
                Error <= 1;
            end else begin
                Error <= 0;
            end
            if (dly == 3'b101) begin
                Found <= 1;
            end else begin
                Found <= 0;
            end
        end
    end

endmodule
```

> *Explanation:* From theory we know that a signal generates a flip-flop whenever an assignement is made at the transition of another signal; a synchronous assignement. In the code above we see that inside the clocked process, there are assignments to signals cnt (9 bits), dly (3 bits), Error (1 bit) and Found (1 bit). Hence, the answer is 14. 

- [ ] 0
- [ ] 2
- [ ] 3
- [ ] 8
- [ ] 9
- [ ] 12
- [x] 14
- [ ] 128
- [ ] 264


### Question 3
**What is the largest value the cnt signal can store?**
```
module Matcher (
    input logic Clk,
    input logic Rst,
    input logic DataIn,
    output logic Error,
    output logic Found
);

logic [8:0] cnt;
logic [2:0] dly;

    always @(posedge clk) begin
        if (Rst) begin
            dly <= 0;
            cnt <= 0;
            Error <= 0;
            Found <= 0;
        end else begin
            dly[0] <= DataIn;
            dly[1] <= dly[0];
            dly[2] <= dly[1];
            cnt <= cnt + 1;
            if (cnt == 128) begin
                Error <= 1;
            end else begin
                Error <= 0;
            end
            if (dly == 3'b101) begin
                Found <= 1;
            end else begin
                Found <= 0;
            end
        end
    end
    
endmodule
```

- [ ] 8
- [ ] 9
- [ ] 128
- [ ] 255
- [ ] 256
- [x] 511
- [ ] 512

> *Explanation:* If a signal has n bits the largest value tha can have is 2^n - 1. Signal count is 9 bits so the largest value is 2^9 - 1 = 511.
