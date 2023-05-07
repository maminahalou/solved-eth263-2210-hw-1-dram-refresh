Download Link: https://assignmentchef.com/product/solved-eth263-2210-hw-1-dram-refresh
<br>



<h1>1. Critical Paper Reviews</h1>

Please read the guidelines for reviewing papers and check the sample reviews. We also assign you a required reading for this homework. You may access them by <em>simply clicking on the QR codes below or scanning them</em>. We will give out extra credit that is worth 0.5% of your total grade for each good review. If you submit 5 or 6 paper reviews, you will receive 250 or 500 BONUS points on top of 1000 points you may get from paper reviews, respectively (i.e., each additional submission is worth 250 BONUS points).

Guidelines                                     Sample reviews                                 Required Reading

Write an approximately one-page critical review for the following required reading (i.e., Paper #1) and <em>at least </em>3 of the remaining 5 papers (i.e., papers from #2 to #6). A review with bullet point style is more appreciated. Try not to use very long sentences and paragraphs. Keep your writing and sentences simple. Make your points bullet by bullet, as much as possible.

<ol>

 <li>(REQUIRED) Onur Mutlu, “Main Memory Scaling: Challenges and Solution Directions”, Invited Book Chapter in More than Moore Technologies for Next Generation Computer Design, pp. 127-153,</li>

</ol>

Springer, 2015. <a href="https://people.inf.ethz.ch/omutlu/pub/main-memory-scaling_springer15.pdf">https://people.inf.ethz.ch/omutlu/pub/main-memory-scaling_springer15.pdf </a>2. Moscibroda and Mutlu, “Memory Performance Attacks: Denial of Memory Service in Multi-Core Systems,” in Proceedings of the USENIX Security, 2007. <a href="https://people.inf.ethz.ch/omutlu/pub/mph_usenix_security07.pdf">https://people.inf.ethz.ch/omutlu/pub/ </a><a href="https://people.inf.ethz.ch/omutlu/pub/mph_usenix_security07.pdf">mph_usenix_security07.pdf</a>

<ol start="3">

 <li>Liu et al., “RAIDR: Retention-Aware Intelligent DRAM Refresh,” in Proceedings of the International Symposium on Computer Architecture, 2012. <a href="https://people.inf.ethz.ch/omutlu/pub/raidr-dram-refresh_isca12.pdf">https://people.inf.ethz.ch/omutlu/pub/ </a><a href="https://people.inf.ethz.ch/omutlu/pub/raidr-dram-refresh_isca12.pdf">raidr-dram-refresh_isca12.pdf</a></li>

 <li>Liu et al., “An Experimental Study of Data Retention Behavior in Modern DRAM Devices: Implications for Retention Time Profiling Mechanisms”, in Proceedings of the International Symposium on Computer Architecture, 2013. <a href="https://people.inf.ethz.ch/omutlu/pub/dram-retention-time-characterization_isca13.pdf">https://people.inf.ethz.ch/omutlu/pub/dram-retention-time-characterization_isca13.pdf</a></li>

 <li>Kim et al., “Flipping Bits in Memory Without Accessing Them: An Experimental Study of DRAM Disturbance Errors”, in Proceedings of the International Symposium on Computer Architecture, 2014. <a href="https://people.inf.ethz.ch/omutlu/pub/dram-row-hammer_isca14.pdf">https://people.inf.ethz.ch/omutlu/pub/dram-row-hammer_isca14.pdf</a></li>

 <li>Kim et al., “Revisiting RowHammer: An Experimental Analysis of Modern Devices and Mitigation Techniques”, in Proceedings of the International Symposium on Computer Architecture, 2020. <a href="https://people.inf.ethz.ch/omutlu/pub/Revisiting-RowHammer_isca20.pdf">https</a><a href="https://people.inf.ethz.ch/omutlu/pub/Revisiting-RowHammer_isca20.pdf"><sub>:</sub></a></li>

</ol>

<a href="https://people.inf.ethz.ch/omutlu/pub/Revisiting-RowHammer_isca20.pdf">//people.inf.ethz.ch/omutlu/pub/Revisiting-RowHammer_isca20.pdf</a>

<h1>2. Main Memory</h1>

Answer the following questions for a machine that has a 4 GB DRAM main memory system and each row is refreshed every 64 ms.

<ul>

 <li>During standalone runs of two applications (A and B) on the machine, you observe that application A spends a significantly larger fraction of cycles stalling for memory than application B does while both applications have a similar number of memory requests. What might be the reasons for this?</li>

 <li>Application A also consumes a much larger amount of memory energy than application B does. What might be the reasons for this?</li>

 <li>When applications A and B run together on the machine, application A’s performance significantly degrades, while application B’s performance does not degrade as much. Why might this happen?</li>

 <li>The designer decides to use a smarter policy to refresh the memory. A row is refreshed only if it has not been accessed in the past 64 ms. Do you think this is a good idea? Why or why not?</li>

 <li>When this new refresh policy is applied, the refresh energy consumption drops significantly during a run of application B. In contrast, during a run of application A, the refresh energy consumption reduces only slightly. Why might this happen?</li>

</ul>

<h1>3. DRAM Refresh – Utilization</h1>

A memory system has four channels, and each channel has two ranks of DRAM chips. Each memory channel is controlled by a separate memory controller. Each rank of DRAM contains eight banks. A bank contains 32K rows. Each row in one bank is 8KB. The minimum retention time among all DRAM rows in the system is 64 ms. In order to ensure that no data is lost, every DRAM row is refreshed once per 64 ms. Every DRAM row refresh is initiated by a command from the memory controller which occupies the command bus on the associated memory channel for 5 ns and the associated bank for 40 ns. Let us consider a 1.024 second span of time.

We define <em>utilization </em>(of a resource such as a bus or a memory bank) as the fraction of total time for which a resource is occupied by a refresh command.

For each calculation in this section, you may leave your answer in <em>simplified </em>form in terms of powers of 2 and powers of 10.

(a) How many refreshes are performed by the memory controllers during the 1.024 second period in total across all four memory channels?

<ul>

 <li>The system designer wishes to reduce the overhead of DRAM refreshes in order to improve system performance and reduce the energy spent in DRAM. A key observation is that not all rows in the DRAM chips need to be refreshed every 64 ms. In fact, rows need to be refreshed only at the following intervals in this particular system:</li>

</ul>

<table width="261">

 <tbody>

  <tr>

   <td width="148">Required Refresh Rate</td>

   <td width="113">Number of Rows</td>

  </tr>

  <tr>

   <td width="148">64 ms</td>

   <td width="113">25</td>

  </tr>

  <tr>

   <td width="148">128 ms</td>

   <td width="113">29</td>

  </tr>

  <tr>

   <td width="148">256 ms</td>

   <td width="113">all other rows</td>

  </tr>

 </tbody>

</table>

Given this distribution, if all rows are refreshed only as frequently as required to maintain their data, how many refreshes are performed by the memory controllers during the 1.024 second period in total across all four memory channels?

<ul>

 <li>What DRAM data bus utilization is caused by DRAM refreshes in this case?</li>

 <li>The system designer wants to achieve this reduction in refresh overhead by refreshing rows less frequently when they need less frequent refreshes. In order to implement this improvement, the system needs to track every row’s required refresh rate. What is the minimum number of bits of storage required to track this information?</li>

 <li>Assume that the system designer implements an approximate mechanism to reduce refresh rate using Bloom filters, as we discussed in class. One Bloom filter is used to represent the set of all rows which require a 64 ms refresh rate, and another Bloom filter is used to track rows which require a 128 ms refresh rate. The system designer modifies the memory controller’s refresh logic so that on every potential refresh of a row (every 64 ms), it probes both Bloom filters. If either of the Bloom filter probes results in a “hit” for the row address, and if the row has not been refreshed in the most recent length of time for the refresh rate associated with that Bloom filter, then the row is refreshed. (If a row address hits in both Bloom filters, the more frequent refresh rate wins.) Any row that does not hit in either Bloom filter is refreshed at the default rate of once per 256 ms. The false-positive rates for the two Bloom filters are as follows:</li>

</ul>

<table width="243">

 <tbody>

  <tr>

   <td width="116">Refresh Rate Bin</td>

   <td width="127">False Positive Rate</td>

  </tr>

  <tr>

   <td width="116">64 ms</td>

   <td width="127">2−20</td>

  </tr>

  <tr>

   <td width="116">128 ms</td>

   <td width="127">2−8</td>

  </tr>

 </tbody>

</table>

The distribution of required row refresh rates specified in part (e) still applies.

How many refreshes are performed by the memory controllers during the 1.024 second period in total across all four memory channels?

<ol start="4">

 <li>RowHammer [150 points]</li>

</ol>

4.1. RowHammer Attacks

In order to characterize the vulnerability of your DRAM device to RowHammer attacks, you must be able to induce RowHammer errors. Assume the following about the target system:

<ul>

 <li>The CPU has a single in-order processor, and does not implement virtual memory.</li>

 <li>The physical memory address is 16 bits.</li>

 <li>The DRAM subsystem consists of two channels, four banks per channel, and 64 rows per bank.</li>

 <li>The memory controller employs open-page policy.</li>

 <li>The DRAM modules and the memory controller do not employ any remapping or scrambling schemes for the physical address.</li>

 <li>All the cells in the DRAM subsystem are equally vulnerable to RowHammer-induced errors.</li>

</ul>

You implement codes based on instructions shown in Table 1.

<table width="485">

 <tbody>

  <tr>

   <td width="107">Instruction</td>

   <td width="147">Description</td>

   <td width="232">Functionality</td>

  </tr>

  <tr>

   <td width="107">B LABEL</td>

   <td width="147">Unconditional Branch</td>

   <td width="232">PC = LABEL</td>

  </tr>

  <tr>

   <td width="107">STORE IMM, Rs</td>

   <td width="147">Store word to memory</td>

   <td width="232">MEM[IMM] = Rs</td>

  </tr>

  <tr>

   <td width="107">CLFLUSH IMM</td>

   <td width="147">Cache line flush</td>

   <td width="232">Flush cache line containing IMM</td>

  </tr>

 </tbody>

</table>

<strong>Table 1. Instruction Descriptions.</strong>

<ul>

 <li>You run Code 1 below, but you cannot observe any errors in the target system. You figured out that the number of activations is much lower than your expectation. Give reason(s) as to why Code 1 cannot introduce a sufficient amount of activations.</li>

</ul>

Code 1 1: LOOP:

2:             STORE0x8732, R0

<ul>

 <li>You try Codes 2a, 2b, and 2c, but find that <em>only one of them can induce RowHammer errors </em>in your DRAM subsystem. Which code segment is the one that can induce RowHammer errors? Justify your</li>

</ul>




<table width="556">

 <tbody>

  <tr>

   <td width="198">Code 2a1: LOOP:2:                STORE0x8732, R03:                STORE0x98CD, R14:               CLFLUSH0x87325:               CLFLUSH0x98CD6:              BLOOP</td>

   <td width="198">Code 2b1: LOOP:2:                STORE0xF1AB, R03:                STORE0x0054, R14:               CLFLUSH0xF1AB5:               CLFLUSH0x00546:              BLOOP</td>

   <td width="160">Code 2c1: LOOP:2:                  STORE0x2B97, R03:                 STORE0xDA68, R14:               CLFLUSH0x2B975:               CLFLUSH0xDA686:              BLOOP</td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="32"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

answer.

4.2. RowHammer Mitigation Mechanisms

To identify a viable RowHammer mitigation mechanism for your system, you compare the two following mitigation mechanisms:

<ul>

 <li><strong>Mechanism A. </strong>The memory controller maintains a counter for every row, which increments every time the corresponding row is activated. If the counter value for a row exceeds a threshold value <em>T</em>, the memory controller activates the row’s two adjacent rows and resets the counter.</li>

 <li><strong>Mechanism B. </strong>Each time a row is closed (or precharged), the memory controller flips a biased coin with a probability <em>p </em>of turning up heads, where <em>p &lt;&lt; </em>1. If the coin turns up heads, the memory controller activates one of its adjacent rows where either of the two adjacent rows are selected with equal probability (<em>p/</em>2).</li>

</ul>

<ul>

 <li>You set <em>T </em>for Mechanism A to 164 K based on the value of the Maximum Activation Count (MAC, i.e., the maximum number of times a row can be activated without inducing RowHammer errors in its adjacent rows) reported by the DRAM manufacturer. Calculate the number of bits required for counters in a memory controller which manages a single channel, 2 ranks per channel, 8 banks per rank, and 2<sup>15 </sup>rows per bank.</li>

 <li>How does the answer to (a) change when both the number of rows per bank and the number of banks per chip are doubled?</li>

 <li>You profile the memory access pattern of the target system, and observe that the same pattern repeats exactly every 64 ms (the current refresh interval). Table 2 shows the number of activations for each row within a 64-ms time interval in a descending order. Given values <em>T </em>=164 K for Mechanism A and <em>p </em>= 0<em>.</em>001 for Mechanism B, calculate the expected number of additional activations within a 64-ms time interval under each technique.</li>

</ul>

<table width="177">

 <tbody>

  <tr>

   <td width="89">Row Index</td>

   <td width="89"># of ACTs</td>

  </tr>

  <tr>

   <td width="89">0x7332F</td>

   <td width="89">73 K</td>

  </tr>

  <tr>

   <td width="89">0x1802C</td>

   <td width="89">64 K</td>

  </tr>

  <tr>

   <td width="89">0x03F05</td>

   <td width="89">32 K</td>

  </tr>

  <tr>

   <td width="89">0x5FF02</td>

   <td width="89">10 K</td>

  </tr>

  <tr>

   <td width="89">…</td>

   <td width="89">…</td>

  </tr>

  <tr>

   <td width="89">Total</td>

   <td width="89">480 K</td>

  </tr>

 </tbody>

</table>

<strong>Table 2. Number of Activations for Each Row.</strong>

<h1>5. VRL: Variable Refresh Latency</h1>

In this question, you are asked to evaluate Variable Refresh Latency<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>, which is based on two key observations:

<ul>

 <li>First, a cell’s charge reaches 95% of the maximum charge level in 60% of the nominal latency value during a refresh operation. In other words, the last 40% of the refresh latency is spent to increase the charge of a cell from 95% to 100%.</li>

 <li>Second, a 100% charged cell reliably operates even after several 95% charge restorations, but it needs to be fully charged again after a finite number of 95% charge restorations. This finite number varies from cell to cell.</li>

</ul>

Based on these observations, the paper defines two types of refresh operations: (1) <em>full refresh </em>and (2) <em>partial refresh</em>. Full refresh uses the nominal latency and restores the cell charge to 100%, while the latency of partial refresh is only 60% of the nominal value and it restores 95% of the initial charge level. The key idea of the paper is to apply a <em>full refresh </em>operation only when necessary and use <em>partial refresh </em>operations at all other times.

<ul>

 <li>Consider a case in which:

  <ul>

   <li>Each row must be refreshed every 64 ms (i.e., the refresh interval is 64 ms).</li>

   <li>Row refresh commands are evenly distributed across the refresh interval. In other words, all rows are refreshed exactly once in <em>any </em>given 64 ms time window.</li>

   <li>You are given the following plot, which shows <em>the distribution of the maximum number of partial refreshes </em>across all rows of a particular bank.</li>

   <li>We define T as the time that a bank is busy serving the refresh requests in a window of 64ms. if all rows are always fully refreshed (baseline).</li>

  </ul></li>

</ul>

How much time does it take (in terms of T) for a bank to refresh all rows within a refresh interval after applying Variable Refresh Latency?

<ul>

 <li>You find out that you can relax the refresh interval of the baseline before applying Variable Refresh Latency as follows:

  <ul>

   <li>90% of the rows are refreshed at every 128ms; 10% of the rows are refreshed at every 64ms.</li>

   <li>Refresh commands are evenly distributed in time.</li>

   <li>All rows are always fully refreshed.</li>

   <li>A row’s refresh operation costs 0<em>.</em>2<em>/N ms.</em>, where N is the number of rows in a bank.</li>

  </ul></li>

</ul>

We define <em>refresh overhead </em>as the fraction of time that a bank is busy, serving the refresh requests over a very large period of time. Calculate the refresh overhead for the baseline with the relaxed refresh interval.

<ul>

 <li>Consider a case where:

  <ul>

   <li>90% of the rows are refreshed at every 128ms; 10% of the rows are refreshed at every 64ms.</li>

   <li>Refresh commands are evenly distributed in time.</li>

   <li>You are given the following plot, which shows <em>the distribution of the maximum number of partial refreshes </em>across all rows of a particular bank.</li>

   <li>Fully refreshing a row costs 0<em>.</em>2<em>/N ms.</em>, where N is the number of rows in a bank.</li>

   <li><em>Refresh overhead </em>is defined as the fraction of time that a bank is busy, serving the refresh requests over a very large period of time.</li>

  </ul></li>

</ul>

Calculate the refresh overhead and compare it against the baseline configuration (the previous question). How much reduction do you see in the performance overhead of refreshes?

<h1>6. BONUS: DRAM Refresh – Energy</h1>

A new supercomputer has a DRAM-based memory system with the following configuration:

<ul>

 <li>The total capacity is 1 ExaByte (EB).</li>

 <li>The DRAM row size is 8 KiloByte (KB).</li>

 <li>The minimum retention time among all DRAM rows in the system is 64 ms. In order to ensure that no data is lost, every DRAM row is refreshed once every 64 ms. (Note: For each calculation in this question, you may leave your answer in simplified form in terms of powers of 2 and powers of 10.) (a) How many DRAM rows does the memory system have?</li>

</ul>

(c) What is the power consumption of DRAM refresh? (Hint: you will need to figure out how much current the DRAM device draws during refresh operations. You can find useful information in the technical note by Micron<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a>. Use the current (IDD) numbers specified in Micron’s datasheet<sup>3</sup>.

Clearly state all the assumptions and show how you derive the power numbers. You are welcome to use other datasheets as well. Make sure you specify how you obtain the power numbers and show your calculations and thought process.)

<a href="#_ftnref1" name="_ftn1">[1]</a> Das et al., <em>“VRL-DRAM: Improving DRAM Performance via Variable Refresh Latency.” </em>In Proceedings of the 55th Annual Design Automation Conference (DAC), 2018.

<a href="#_ftnref2" name="_ftn2">[2]</a> <a href="https://safari.ethz.ch/digitaltechnik/spring2019/lib/exe/fetch.php?media=tn4704.pdf">Micron, “TN-47-04: Calculating Memory System Power for DDR2 Introduction” </a><a href="https://safari.ethz.ch/digitaltechnik/spring2019/lib/exe/fetch.php?media=1gb_ddr3_sdram.pdf"><sup>3</sup></a><a href="https://safari.ethz.ch/digitaltechnik/spring2019/lib/exe/fetch.php?media=1gb_ddr3_sdram.pdf">Micron, “1Gb: x4, x8, x16 DDR3 SDRAM Features”</a>