### Question 1
**What type of reset does the following code use?**
```
module FrameChecker (
    input logic Clk,
    input logic Rst,
    input logic StartIn,
    input logic EndIn,
    output logic ErrorOut
);

    typedef enum {sReset, sIdle, iActive} StateType;
    StateType sState;
    
    always @(posedge Clk or posedge Rst) begin
        if (Rst) begin
            ErrorOut <= 0;
            sState <= sReset;
        end else begin
            ErrorOut <= 0;
            case (sState)
                sReset : begin
                    sState <= sIdle;
                end
                sIdle : begin
                    if (StartIn) begin
                        sState <= iActive;
                    end
                end
                iActive : begin
                    if (EndIn) begin
                        sState <= sIdle;
                    end
                    if (StartIn) begin
                        ErrorOut <= 1;
                    end
                end
            endcase
        end
    end
endmodule
```

- [x] asyncrhonous
- [ ] synchronous

### Question 2
**How many registers would it take to implement the FrameChecker module if the state machine uses one-hot encoding?**
```
module FrameChecker (
    input logic Clk,
    input logic Rst,
    input logic StartIn,
    input logic EndIn,
    output logic ErrorOut
);

    typedef enum {sReset, sIdle, iActive} StateType;
    StateType sState;
    
    always @(posedge Clk or posedge Rst) begin
        if (Rst) begin
            ErrorOut <= 0;
            sState <= sReset;
        end else begin
            ErrorOut <= 0;
            case (sState)
                sReset : begin
                    sState <= sIdle;
                end
                sIdle : begin
                    if (StartIn) begin
                        sState <= iActive;
                    end
                end
                iActive : begin
                    if (EndIn) begin
                        sState <= sIdle;
                    end
                    if (StartIn) begin
                        ErrorOut <= 1;
                    end
                end
            endcase
        end
    end
endmodule
```

- [ ] 0
- [ ] 1
- [ ] 2
- [ ] 3
- [x] 4
- [ ] 5


### Question 3
**How many registers would it take to implement the FrameChecker module if the state machine uses binary encoding?**
```
module FrameChecker (
    input logic Clk,
    input logic Rst,
    input logic StartIn,
    input logic EndIn,
    output logic ErrorOut
);
    
    typedef enum {sReset, sIdle, iActive} StateType;
    StateType sState;
    
    always @(posedge Clk or posedge Rst) begin
        if (Rst) begin
            ErrorOut <= 0;
            sState <= sReset;
        end else begin
            ErrorOut <= 0;
            case (sState)
                sReset : begin
                    sState <= sIdle;
                end
                sIdle : begin
                    if (StartIn) begin
                        sState <= iActive;
                    end
                end
                iActive : begin
                    if (EndIn) begin
                        sState <= sIdle;
                    end
                    if (StartIn) begin
                        ErrorOut <= 1;
                    end
                end
            endcase
        end
    end
endmodule
```


- [ ] 0
- [ ] 1
- [ ] 2
- [x] 3
- [ ] 4
- [ ] 5


### Question 4
**How many registers would it take to implement the FrameChecker module if the state machine uses grey encoding?**
```
module FrameChecker (
    input logic Clk,
    input logic Rst,
    input logic StartIn,
    input logic EndIn,
    output logic ErrorOut
);

    typedef enum {sReset, sIdle, iActive} StateType;
    StateType sState;

    always @(posedge Clk or posedge Rst) begin
        if (Rst) begin
            ErrorOut <= 0;
            sState <= sReset;
        end else begin
            ErrorOut <= 0;
            case (sState)
                sReset : begin
                    sState <= sIdle;
                end
                sIdle : begin
                    if (StartIn) begin
                        sState <= iActive;
                    end
                end
                iActive : begin
                    if (EndIn) begin
                        sState <= sIdle;
                    end
                    if (StartIn) begin
                        ErrorOut <= 1;
                    end
                end
            endcase
        end
    end
endmodule
```


- [ ] 0
- [ ] 1
- [ ] 2
- [x] 3
- [ ] 4
- [ ] 5


### Question 5
**What encoding technique is best if you want to minimize state register transitions?**
```
module FrameChecker (
    input logic Clk,
    input logic Rst,
    input logic StartIn,
    input logic EndIn,
    output logic ErrorOut
);

    typedef enum {sReset, sIdle, iActive} StateType;
    StateType sState;

    always @(posedge Clk or posedge Rst) begin
        if (Rst) begin
            ErrorOut <= 0;
            sState <= sReset;
        end else begin
            ErrorOut <= 0;
            case (sState)
                sReset : begin
                    sState <= sIdle;
                end
                sIdle : begin
                    if (StartIn) begin
                        sState <= iActive;
                    end
                end
                iActive : begin
                    if (EndIn) begin
                        sState <= sIdle;
                    end
                    if (StartIn) begin
                        ErrorOut <= 1;
                    end
                end
            endcase
        end
    end
endmodule
```

- [ ] binary
- [ ] one-hot
- [x] gray


### Question 6
**Which encoding technique produces the least amount of logic on generating the ErrorOut signal?**
```
module FrameChecker (
    input logic Clk,
    input logic Rst,
    input logic StartIn,
    input logic EndIn,
    output logic ErrorOut
);

    typedef enum {sReset, sIdle, iActive} StateType;
    StateType sState;

    always @(posedge Clk or posedge Rst) begin
        if (Rst) begin
            ErrorOut <= 0;
            sState <= sReset;
        end else begin
            ErrorOut <= 0;
            case (sState)
                sReset : begin
                    sState <= sIdle;
                end
                sIdle : begin
                    if (StartIn) begin
                        sState <= iActive;
                    end
                end
                iActive : begin
                    if (EndIn) begin
                        sState <= sIdle;
                    end
                    if (StartIn) begin
                        ErrorOut <= 1;
                     end
                end
            endcase
        end
    end
endmodule
```


- [ ] binary
- [x] one-hot
- [ ] gray
