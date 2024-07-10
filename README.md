# Codtech-Task-1
// VERILOG CODE AND TESTBENCH FOR OR GATE //

module myorgate (
    input A,
    input B,
    output Y
);
    assign Y = A | B;
endmodule

//////TESTBENCH/////

module test_myorgate;
    reg A;
    reg B;
    wire Y;

    // Instantiate the OR gate
    myorgate uut (
        .A(A),
        .B(B),
        .Y(Y)
    );

    initial begin
        // Apply test vectors
        A = 0; B = 0; #10;
        A = 0; B = 1; #10;
        A = 1; B = 0; #10;
        A = 1; B = 1; #10;
        $finish;
    end
endmodule
_____________________________________________________________________________________________________


// VERILOG CODE AND TESTBENCH  FOR AND GATE //


module myandgate (
input A,
input B,
output Y
);
assign Y = A & B;
endmodule
////////////// TESTBENCH /////////////////
module test_myandgate;
reg A;
reg B;
wire Y;
// Instantiate the AND gate
myandgate uut (
.A(A),
.B(B),
.Y(Y)
);
initial begin
// Display the header for the waveform 
output
$display("A B | Y");
$display("------");
// Apply test vectors
A = 0; B = 0; #10;
$display("%b %b | %b", A, B, Y);
A = 0; B = 1; #10;
$display("%b %b | %b", A, B, Y);
A = 1; B = 0; #10;
$display("%b %b | %b", A, B, Y);
A = 1; B = 1; #10;
$display("%b %b | %b", A, B, Y);
$finish;
end
endmodule

______________________________________________________________________________________________________________

//VERILOG CODE AND TESTBENCH FOR NOT GATE//

module mynotgate (
    input A,
    output Y
);
    assign Y = ~A;
endmodule
//////////////  TESTBENCH  /////////////////
module test_mynotgate;
    reg A;
    wire Y;

    // Instantiate the NOT gate
    mynotgate uut (
        .A(A),
        .Y(Y)
    );

    initial begin
        // Display the header for the waveform output
        $display("A | Y");
        $display("----");

        // Apply test vectors
        A = 0; #10;
        $display("%b | %b", A, Y);

        A = 1; #10;
        $display("%b | %b", A, Y);

        $finish;
    end
endmodule

___________________________________________________________________________________________________________________

//VERILOG CODE AND TESTBENCH FOR NOR GATE//

module mynorgate (
    input A,
    input B,
    output Y
);
    assign Y = ~(A | B);
endmodule


////////////   TESTBENCH   ////////////

module test_mynorgate;
    reg A;
    reg B;
    wire Y;

    // Instantiate the NOR gate
    mynorgate uut (
        .A(A),
        .B(B),
        .Y(Y)
    );

    initial begin
        // Display the header for the waveform output
        $display("A B | Y");
        $display("----|--");

        // Apply test vectors
        A = 0; B = 0; #10;
        $display("%b %b | %b", A, B, Y);

        A = 0; B = 1; #10;
        $display("%b %b | %b", A, B, Y);

        A = 1; B = 0; #10;
        $display("%b %b | %b", A, B, Y);

        A = 1; B = 1; #10;
        $display("%b %b | %b", A, B, Y);

        $finish;
    end
endmodule

_______________________________________________________________________________________________________________

//VERILOG CODE AND TESTBENCH FOR NAND GATE //

module mynandgate (
    input A,
    input B,
    output Y
);
    assign Y = ~(A & B);
endmodule

///////////TESTBENCH/////////////

module test_mynandgate;
    reg A;
    reg B;
    wire Y;

    // Instantiate the NAND gate
    mynandgate uut (
        .A(A),
        .B(B),
        .Y(Y)
    );

    initial begin
        // Display the header for the waveform output
        $display("A B | Y");
        $display("----|--");

        // Apply test vectors
        A = 0; B = 0; #10;
        $display("%b %b | %b", A, B, Y);

        A = 0; B = 1; #10;
        $display("%b %b | %b", A, B, Y);

        A = 1; B = 0; #10;
        $display("%b %b | %b", A, B, Y);

        A = 1; B = 1; #10;
        $display("%b %b | %b", A, B, Y);

        $finish;
    end
endmodule

______________________________________________________________________________________________

// VERILOG CODE AND TESTBENCH FOR XOR GATE //

module myxorgate (
input A,
input B,
output Y
);
assign Y = A ^ B;
endmodule

////////////TESTBENCH//////////////


module test_myxorgate;
reg A;
reg B;
wire Y;
// Instantiate the XOR gate
myxorgate uut (
.A(A),
.B(B),
.Y(Y)
);
initial begin
// Display the header for the waveform 
output
$display("A B | Y");
$display("------");
// Apply test vectors
A = 0; B = 0; #10;
$display("%b %b | %b", A, B, Y);
A = 0; B = 1; #10;
$display("%b %b | %b", A, B, Y);
A = 1; B = 0; #10;
$display("%b %b | %b", A, B, Y);
A = 1; B = 1; #10;
$display("%b %b | %b", A, B, Y);
$finish;
end
endmodule

_________________________________________________________________________________________________________________

// VERILOG CODE AND TESTBENCH FOR XNOR GATE //

module myxnorgate (
    input A,
    input B,
    output Y
);
    assign Y = ~(A ^ B);
endmodule

//////////TESTBENCH////////////

module test_myxnorgate;
    reg A;
    reg B;
    wire Y;

    // Instantiate the XNOR gate
    myxnorgate uut (
        .A(A),
        .B(B),
        .Y(Y)
    );

    initial begin
        // Display the header for the waveform output
        $display("A B | Y");
        $display("----|--");

        // Apply test vectors
        A = 0; B = 0; #10;
        $display("%b %b | %b", A, B, Y);

        A = 0; B = 1; #10;
        $display("%b %b | %b", A, B, Y);

        A = 1; B = 0; #10;
        $display("%b %b | %b", A, B, Y);

        A = 1; B = 1; #10;
        $display("%b %b | %b", A, B, Y);

        $finish;
    end
endmodule

_____________________________________________________________________________________________________

// VERILOG CODE AND TESTBENCH FOR HALF ADDER //


module myhalfadder (
input A,
input B,
output Sum,
output Carry
);
assign Sum = A ^ B;
assign Carry = A & B;
endmodule


/////////TESTBENCH///////////


module test_myhalfadder;
reg A;
reg B;
wire Sum;
wire Carry;
// Instantiate the half adder
myhalfadder uut (
.A(A),
.B(B),
.Sum(Sum),
.Carry(Carry)
);
initial begin
// Display the header for the waveform 
output
$display("A B | Sum Carry");
$display("----|----------");
// Apply test vectors
A = 0; B = 0; #10;
$display("%b %b | %b %b", A, B, Sum, 
Carry);
A = 0; B = 1; #10;
$display("%b %b | %b %b", A, B, Sum, 
Carry);
A = 1; B = 0; #10;
$display("%b %b | %b %b", A, B, Sum, 
Carry);
A = 1; B = 1; #10;
$display("%b %b | %b %b", A, B, Sum, 
Carry);
$finish;
end
endmodule

______________________________________________________________________________________________

// VERILOG CODE AND TESTBENCH FOR FULL ADDER //



module myfulladder (
input A,
input B,
input Cin,
output Sum,
output Cout
);
assign Sum = A ^ B ^ Cin;
assign Cout = (A & B) | (Cin & (A ^ B));
endmodule


///////// --- TESTBENCH  ---  //////////


module test_myfulladder;
reg A;
reg B;
reg Cin;
wire Sum;
wire Cout;
// Instantiate the full adder
myfulladder uut (
.A(A),
.B(B),
.Cin(Cin),
.Sum(Sum),
.Cout(Cout)
);
initial begin
// Display the header for the waveform 
output
$display("A B Cin | Sum Cout");
$display("--------|----------");
// Apply test vectors
A = 0; B = 0; Cin = 0; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 0; B = 0; Cin = 1; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 0; B = 1; Cin = 0; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 0; B = 1; Cin = 1; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 1; B = 0; Cin = 0; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 1; B = 0; Cin = 1; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 1; B = 1; Cin = 0; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
A = 1; B = 1; Cin = 1; #10;
$display("%b %b %b | %b %b", A, B, 
Cin, Sum, Cout);
$finish;
end
endmodule

____________________________________________________________________________________________

// VERILOG CODE AND TESTBENCH FOR 2 TO 1 MULTIPLEXER //



module my2to1mux (
    input A,
    input B,
    input Sel,
    output Y
);
    assign Y = (Sel) ? B : A;
endmodule

//////////////////  TESTBENCH  ///////////////////////

module test_my2to1mux;
    reg A;
    reg B;
    reg Sel;
    wire Y;

    // Instantiate the 2-to-1 multiplexer
    my2to1mux uut (
        .A(A),
        .B(B),
        .Sel(Sel),
        .Y(Y)
    );

    initial begin
        // Display the header for the waveform output
        $display("A B Sel | Y");
        $display("--------|--");

        // Apply test vectors
        A = 0; B = 0; Sel = 0; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 0; B = 0; Sel = 1; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 0; B = 1; Sel = 0; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 0; B = 1; Sel = 1; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 1; B = 0; Sel = 0; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 1; B = 0; Sel = 1; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 1; B = 1; Sel = 0; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        A = 1; B = 1; Sel = 1; #10;
        $display("%b %b  %b  | %b", A, B, Sel, Y);

        $finish;
    end
endmodule

Name:MUSKAN KUMARI
<br>
Company:CODTECH IT SOLUTIONS
<br>
ID:CT4VLSI2707
<br>
Domain:VLSI
<br>
Duration:June to July 2024
<br>
Mentor:SRAVANI GOUNI
<br>

Project Overview:
<br>

Objective:
<br>
Design, implement, and simulate fundamental digital circuits using Verilog HDL and ModelSim software, demonstrating a thorough understanding of digital logic design principles.
<br>
Key Activities:
<br>

- Mastering Verilog HDL: Grasp the syntax and semantics of Verilog, including modules, ports, wires, and registers.<br>

- Implementing Logic Gates: Design and develop various basic logic gates (AND, OR, NOT, NAND, NOR, XOR, XNOR) using Verilog.<br>

- Designing Combinational Circuits: Build more complex circuits using basic gates, including half adders, full adders, and multiplexers.<br>

- Creating Testbenches: Develop testbenches for each logic gate and combinational circuit, applying various input combinations to verify correct functionality.<br>

- Simulation and Verification: Compile Verilog code, run simulations in ModelSim, and analyze waveforms to ensure circuit functionality.<br>

- Debugging and Validation: Identify and fix errors, verifying circuit correctness through simulation and comparison with expected results.<br>

Project Components:<br>

- Logic Gate Modules: Implement each gate as a separate Verilog module (e.g., my_and_gate, my_or_gate, etc.).<br>

- Combinational Circuit Modules: Implement more complex circuits using multiple logic gates (e.g., my_half_adder, my_full_adder, etc.).<br>

- Testbenches: Develop testbenches for each module, applying various input combinations and checking outputs.<br>

Skills and Tools Used:<br>

- Verilog HDL: Write efficient and syntactically correct Verilog code, demonstrating an understanding of digital logic design principles.<br>

- ModelSim: Compile and simulate Verilog code, using waveform viewers to analyze circuit behavior.<br>

- Debugging and Verification: Identify and fix errors, verifying circuit correctness through simulation and comparison with expected results.<br>

Project Summary:<br>
This project demonstrates the ability to design and implement digital logic circuits using Verilog HDL, validating designs through simulation in ModelSim. Hands-on experience is gained through writing testbenches and analyzing waveforms, developing a solid foundation in digital design and simulation. The importance of verification and debugging in the design process is highlighted, ensuring final circuits perform as intended.<br>



![verilog01](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/9c393887-dd5b-4997-ae98-0953cb7c02aa)

![verilog1](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/165e6cb6-21dc-40fd-9994-b496537afafd)

![verilog02](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/cb38e3a4-90bc-4168-a415-27ab4d63edfc)

![verilog2](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/655012e5-c788-4f36-8e21-ed32130b80da)

![verilog03](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/3c4fc9a8-1ccd-422f-8717-3c96aa256250)

![verilog3](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/c30b7f09-fc0b-44fb-84fd-25504c334585)

![verilog4](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/3eaf9781-6643-4e81-a1c1-66c7e369f21f)

![verilog5](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/fb3651ee-4647-48cf-98e1-9930877c83f2)

![verilog6](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/2db884f8-04ff-4b7b-ad54-f64bbbb752ae)

![verilog7](https://github.com/mk3271227/Codtech-Task-1/assets/175197452/8e85de24-59dd-4f17-9e47-2db0686c9132)
