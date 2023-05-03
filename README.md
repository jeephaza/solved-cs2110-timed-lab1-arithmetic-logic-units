Download Link: https://assignmentchef.com/product/solved-cs2110-timed-lab1-arithmetic-logic-units
<br>
In this timed lab, you will be creating an ALU. This ALU will take in <strong>two 8-bit inputs </strong>and <strong>one 2-bit select bit</strong>. It will output <strong>one 8-bit output</strong>.

When building this ALU, you may only use basic logic gates (AND, OR, NAND, NOR, NOT), decoders, multiplexers, adders, splitters, wires, tunnels, constants, input pins, and output pins. <strong>YOU DO NOT</strong>

<strong>NEED TO BUILD THE GATES OUT OF TRANSISTORS. PLEASE, FOR YOUR OWN SAKE, DON’T DO IT</strong>.

<strong>IMPORTANT NOTE: </strong>You probably did not really read the paragraph above, but it says you’re allowed to use CircuitSim’s default adders (in the Arithmetic tab). So please don’t try to make your own adders, just use that one. You’re not allowed to use anything else from the Arithmetic tab (don’t try to be smart and use a subtractor).

Some operations will also have additional banned operations.

<h1><a name="_Toc3247"></a>3           Instructions</h1>

Please make sure that you have <strong>CircuitSim 1.7.4 or 1.8.0 </strong>installed on your computer. All changes should be made in the <em>tl1.sim </em>file. Do not move or rename any or the input or output pins.

You will create an 8-bit ALU with the following operations, using any of the gates listed above. All numbers should be interpreted as 2’s complement.

<table width="603">

 <tbody>

  <tr>

   <td width="213">00. Is Multiple of 16</td>

   <td width="391">[A % 16 == 0]</td>

  </tr>

  <tr>

   <td width="213">01. 4A-B</td>

   <td width="391">[4A – B] <em>you may only use one adder</em></td>

  </tr>

  <tr>

   <td width="213">10. !A &amp;&amp; B</td>

   <td width="391">[!A &amp;&amp; B] <strong>Note: this is a logical AND! Clarification below.</strong></td>

  </tr>

  <tr>

   <td width="213">11. Multiply by 12</td>

   <td width="391">[A * 12] <em>you may only use one adder</em></td>

  </tr>

 </tbody>

</table>

Notice that Is Multiple of 16, and Multiply by 12 only operate on the A input. <strong>They should NOT rely on </strong>B <strong>being a particular value.</strong>

Notice that opcode 10 applies a logical AND. This operation is equivalent to the following ternary expression:

(A == 0 &amp;&amp; B != 0) ? 1 : 0. That is, your circuit should output 00000001 if A is zero and B is not zero. Otherwise, it should output 00000000. <em>Hint: You can check if a number is zero by NORing its bits.</em>

This ALU has two <strong>8-bit </strong>inputs for A and B and one <strong>2-bit </strong>input for OP, the op-code for the operation in the list above. It has one <strong>8-bit </strong>output named OUT.

The provided autograder will check the op-codes according to the order listed above (Is Multiple of 16 (000), 4A-B (001), etc.) and thus it is important that the operations are in this exact order.

<h1><a name="_Toc3248"></a>4           Deliverables</h1>

Please upload the following files onto the assignment on Gradescope:

<ol>

 <li>tl1.sim</li>

</ol>