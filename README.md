Download Link: https://assignmentchef.com/product/solved-cs223-laboratory-assignment-5-reduce-sum-on-array
<br>



This lab will be performed online through Zoom.







This lab, you are asked to implement a HLSM that will sum all the elements of an array. The array should be implemented as a RAM which can hold at most 16 elements, where each element is 8-bits. The RAM you implement must have the following inputs: clock, writeAddress, writeData, writeEnable, readAddress1, readAddress2, readData1, readData2. You will use switches to enter data, where the SW[7:0] (8 leftmost switches) would define the data to enter and SW[15:12] would define the address in memory. When the uppermost pushbutton is pressed, data defined by switches will be written to the specified address of the memory. Left and right pushbuttons will be used to circulate and show the specified memory address and data on seven-segment display. Middle pushbutton will calculate the sum and show it on LEDs. You will be given the seven-segment display and debouncer for pushbutton modules. One of the read ports of the RAM will be connected to seven-segment display to show the data, and the other one will be connected to reduce sum module which will calculate the sum of all elements. In the Seven-Segment Display, the most significant digit will show the current address to display, and the least significant 2 digits will show the data in that address. The remaining digit in between should be turned off.




Figure 1: Flow Architecture

For the example memory given in Figure 1, if the memory address 0 is displayed, seven segment will show “0 0A,” if then display previous data button is pressed, “F 00” should be displayed. If Run Reduce Sum button is pressed, the leds will show 0x5B in binary as the sum. Assuming input address switches are “1111” and input data to memory switches are also all on, when display enter data to memory button is pressed, the seven segment should now show “F FF” as adress 0xF was being displayed and the data is updated to “0xFF” now. LEDs will not change until Run Reduce Sum button is pressed again.

<h1>Preliminary Report (45 points)</h1>

Today’s lab needs considerable advance preparation. These advance designs and SystemVerilog models should be prepared in advance, and assembled neatly into a Preliminary Report with a cover page and pages for the SystemVerilog codes. Each page should have a proper heading. The report should be uploaded on Moodle as a pdf file before the start of the lab. The content of the report will be as follows:

<ol>

 <li>Show the ReduceSum HLSM. Show also the controller/datapath diagram for it.</li>

 <li>You will be given a debouncer module for your pushbuttons. Research and explain briefly why there is a need for such a circuit.</li>

 <li>Write the SystemVerilog Code for your memory module. Write a testbench for it.</li>

 <li>Write the SystemVerilog Code for your ReduceSum Module. Write a testbench for it.</li>

 <li>Write the SystemVerilog Code for the top design which will also include the Seven Segment Display and debouncer modules.</li>

</ol>

<strong> </strong>

<h1>Simulation (20 Points)</h1>

Enter System Verilog module for your ReduceSum module and run your testbench for it. Show your simulation to TA.

<h1>Implementation on FPGA (35 Points)</h1>

In this part you are going to implement your overall module on FPGA and have a demo.

<ul>

 <li>Right and left pushbuttons will be used to circulate in memory. Initial address will be 0. If right pushbutton is pressed the data on address 1 should be displayed. Then if again the right pushbutton is pressed data on address 2 should be displayed an so on. If left pushbutton is pressed while address is 0, data on address 15 should be displayed.</li>

 <li>When the upper pushbutton is pressed, the data on SW[7:0] should be put in address SW[15:12]. Initally, all the values should be 0 in memory.</li>

 <li>With the press on middle pushbutton, the ReduceSum should be calculated and and the result should be displayed on LEDs.</li>

</ul>

Now test your code and show the result to your TA.




<h1>Submit your code for MOSS similarity testing</h1>

Finally, when you are done and before leaving the lab, you need to copy all the SystemVerilog codes you wrote to a txt file named <em><u>StudentID_name.txt</u></em> and upload it to Moodle. If you have multiple files, just copy and paste them in order, one after another inside text file. Even if you didn’t finish or didn’t get the SystemVerilog part working, you must submit your code to the Moodle for similarity checking. Your codes will be compared against all the other codes in all sections of the class, by the MOSS program, to determine how similar it is (as indication of plagiarism). So be sure that the code you submit is the code that you actually wrote yourself!  <strong> </strong>

<strong>Clean Up! </strong>

<ul>

 <li>Clean up your lab station, and return all the parts, wires, the Beti trainer board, etc. Leave your lab workstation.</li>

 <li>CONGRATULATIONS! You are finished with this lab and are one step closer to becoming a computer engineer.</li>

</ul>

<strong>NOTES </strong>

–Advance work on this lab, and all labs, is strongly suggested.

–Be sure to read and follow the Policies for CS223 labs, posted in Unilica.

<ol>

 <li></li>

</ol>