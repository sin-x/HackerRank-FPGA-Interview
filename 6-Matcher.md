##### 1) What type of reset does the following code use?
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

- [ ] synchronous
- [ ] asynchronous



##### 2) How many registers does this design use?
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

- [ ] 0
- [ ] 2
- [ ] 3
- [ ] 8
- [ ] 9
- [ ] 12
- [ ] 14
- [ ] 128
- [ ] 264



##### 3) What is the largest value the cnt signal can store?
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
- [ ] 511
- [ ] 512
