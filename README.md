Download Link: https://assignmentchef.com/product/solved-cpe301-lab-05-timers-in-computer-applications
<br>
To become familiar with the use of timers in computer applications. Specifically, to implement a piano like keyboard program using the ATmega2560 timer1 in Normal mode and an external speaker.

<strong><em>Procedure:</em></strong>

<ol>

 <li>Write a C program for the Arduino Mega SBC which will monitor the keyboard for inputs of A, B, C,</li>

</ol>

D, E, F, and G. Depending upon which key was pressed <strong>use the timer </strong>to generate a square wave on PortB.6 of the ATmega2560 (Arduino Digital pin 12) of the appropriate frequency for the middle octave of that musical note (see Table). The note should last until another key is pressed, at which time the new note will be played. If the ‘q’ key is pressed the note will stop playing. For debugging purposes, use of the Arduino Serial Library is permitted for this lab. Use the file serial_echo_example.ino as an example of serial I/O.

<strong><u>YOUR C PROGRAM MUST CONTAIN A FUNCTION WHICH TAKES THE FREQUENCY AS</u></strong>

<strong><u>AN INPUT, AND THEN CONFIGURES AND RUNS THE TIMER. THIS FUNCTION MUST</u></strong><strong> <u>WORK FOR ALL NOTES LISTED IN THE TABLE, IT DOES NOT HAVE TO WORK FOR ALL</u> <u>POSSIBLE FREQUENCIES.</u>  </strong>

<ol start="2">

 <li>Connect the lab speakers to PortB.6 and ground to actually play the notes so you can hear them.</li>

</ol>

<strong><u>BE SURE TO ALWAYS DISCONNECT SBC POWER BEFORE CONNECTING OR</u></strong><strong> <u>DISCONNECTING ANYTHING ELSE TO IT.</u></strong>

<ol start="3">

 <li>Connect a sine wave signal generator to one of the lab speakers, set it to one of the musical note frequencies, and listen to it. Compare the sound of this note with the same frequency note generated from the SBC speaker. Explain why they sound different.</li>

</ol>

<table width="0">

 <tbody>

  <tr>

   <td rowspan="13" width="121">NOTEAA#                       B                         middle C             C#DD#E                          F                          F#GG#</td>

   <td width="124"> FREQUENCY</td>

  </tr>

  <tr>

   <td width="124"> 440 Hz</td>

  </tr>

  <tr>

   <td width="124">  466 Hz</td>

  </tr>

  <tr>

   <td width="124">  494 Hz</td>

  </tr>

  <tr>

   <td width="124">  523 Hz</td>

  </tr>

  <tr>

   <td width="124">  554 Hz</td>

  </tr>

  <tr>

   <td width="124">  587 Hz</td>

  </tr>

  <tr>

   <td width="124">  624 Hz</td>

  </tr>

  <tr>

   <td width="124">  659 Hz</td>

  </tr>

  <tr>

   <td width="124">  698 Hz</td>

  </tr>

  <tr>

   <td width="124">  740 Hz</td>

  </tr>

  <tr>

   <td width="124">  784 Hz</td>

  </tr>

  <tr>

   <td width="124"> 831 Hz</td>

  </tr>

 </tbody>

</table>




The sharp notes are included in the table for completeness. If you choose to implement all of the notes including sharps you will need to decide on an interface protocol which will distinguish between regular and sharp notes. For example, you might define regular notes as upper or lower case and sharps as the opposite.

<strong>If you choose to implement all of the notes you will receive up to 50 points (on a scale of 100) extra credit on this lab.</strong>




HINT:  You can probably write a single subroutine which outputs the notes and checks for input. Then, you can call this single subroutine with different timer “load” values for the different