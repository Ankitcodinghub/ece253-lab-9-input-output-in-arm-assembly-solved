# ece253-lab-9-input-output-in-arm-assembly-solved
**TO GET THIS SOLUTION VISIT:** [ECE253 Lab 9-Input/Output in ARM assembly Solved](https://www.ankitcodinghub.com/product/ece253-lab-9-input-output-in-arm-assembly-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94374&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE253 Lab 9-Input\/Output in ARM assembly Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
The purpose of this lab is to:

1. learn how to interact with memory-mapped devices 2. learn how to use polling to detect external events

1 Preparation

Please refer to the Lab 7 handout for resources related to the ARM processor and the cpulator simulator.

Note: This lab will be marked entirely in-person during your scheduled practical session via a demo to your TA. There is no automarker for this lab.

2 PartI

Write an assembly-language program that turns on two LEDR lights at a time on the DE1- SoC board. First, the lights LEDR9 and LEDR0 should be on, then LEDR8 and LEDR1, then LEDR7 and LEDR2, and so on. When you get to LEDR5 and LEDR4 being on, the direction should be reversed. Only two LEDR lights are ever on at one time. The effect should be a two lights sweeping first towards the centre, then outwards towards the edges, and so on.

Use a delay so that lights move every 0.25 seconds. To implement the delay, use the MP- CORE Private Timer described in the lectures (and also in Section 2.4.1 of the Intel doc- umentation on the Quercus website.) When KEY3 is pressed and released, the sweeping motion should stop. Pressing and releasing KEY3 again should restart the motion of the LEDR lights from where they left off. When the restart occurs, the current LEDRs should remain on for a delay of 0.25s before continuing their motion.

To synchronize with the timer device in your main program, use polled I/O by repeatedly reading the F bit in the timer’s status register. Also use polled I/O to deal with the push button KEY3.

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
3

</div>
</div>
<div class="layoutArea">
<div class="column">
1. 2. 3.

</div>
<div class="column">
All necessary code should be contained in one file: part1.s.

You should test your code using the CPUlator simulator or using the DE1-SoC board. There is no tester provided for Part 1.

Part II – Optional for bonus marks

</div>
</div>
<div class="layoutArea">
<div class="column">
In Part I, you used the timer to create a delay, and used polled I/O to synchronize with the timer. Also, you used polled I/O to check when KEY3 was pressed. In this part of the exercise, you are to create the same application, but relying entirely on interrupts instead of polled I/O. Both the timer and the KEY need to be handled through Interrupts.

You are given template code on Quercus called part2 template.s. There is a LOT of code here. At the top of the file you will see a number of .equ lines. These are similar to #define in C and can be used as a convenience for you in your code if you wish.

You will need to fill in the missing parts including:

<ul>
<li>Provide code for all exception handlers. Specifically look for “FILL IN CODE HERE”</li>
<li>Complete the code for the PRIV TIMER ISR. It has to modify the global variables LEDR DIRECTION and LEDR PATTERN that are declared in the main program below. The first of these variables specifies if the LEDR lights are currently sweeping to the centre or to the outside, and the second variable sets which lights are currently turned on.</li>
<li>Complete the code for KEY ISR. This is the push button KEY interrupt service rou- tine. It has to stop and resume the timer when KEY3 is pressed.</li>
<li>Test your code in the cpulator simulator or the DE1-SoC board. No autotester is provided.</li>
<li>You should comment your code so the TA can understand what you are doing.

An outline of the main ( start) program that you need to use for this lab is shown below.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>  .text
  .global _start
</pre>
_start:

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
<pre>  ...initialize the IRQ stack pointer ...
  ...initialize the SVC stack pointer ...
</pre>
<pre>  BL CONFIG_GIC // configure the ARM generic interrupt controller
  BL CONFIG_PRIV_TIMER // configure the MPCore private timer
  BL CONFIG_KEYS // configure the pushbutton KEYs
</pre>
<pre>  ...enable ARM processor interrupts ...
  LDR R6, =0xFF200000 // red LED base address
</pre>
<pre>MAIN:
  LDR R4, LEDR_PATTERN // LEDR pattern; modified by timer ISR
  STR R4, [R6] // write to red LEDs
  B MAIN
</pre>
<pre>/* Configure the MPCore private timer to create interrupts every 0.25 second */
</pre>
<pre>CONFIG_PRIV_TIMER:
  LDR R0, =0xFFFEC600 // Timer base address
  ...code not shown
  MOV PC, LR // return
</pre>
<pre>/* Configure the KEYS to generate an interrupt */
CONFIG_KEYS:
</pre>
<pre>  LDR R0, =0xFF200050 // KEYs base address
  ...code not shown
  MOV PC, LR // return
</pre>
<pre>  .global LEDR_DIRECTION
LEDR_DIRECTION:
</pre>
<pre>  .word 0 // 0 means moving to centre, 1 means moving to outside
</pre>
<pre>  .global LEDR_PATTERN
LEDR_PATTERN:
</pre>
<pre>  .word 0x201 // 1000000001
</pre>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
</div>
