## Introduction
**Cache:** Cache Memory is the CPU fastest accessible memory in CPU. Also, cache is a STATIC RAM. </br>
Cache memory is fastest accessible memory in CPU. The main noticeable feature of cache is its clock speed when compared with RAM (~1600-2100MHz)and HDD(~5400-7200RPM), is comparable to CPU clock speed(~1-4GHz). Maximum transfer rate without RAM and Cache is around 80- 150MBPS. Complexity occurs because of the modern day processors, since they are multi-cored. Cache comes into play here. Cache is also a type of RAM but is called as Static RAM. Typical size of this cache is around kilobytes up to Megabytes in considering its cost and purpose of usage.
<br/>
<br/>

## Idea of this Project

For carrying on this project, Base-delta-immediate cache compression method is studied (different possible cases with differing base
sizes were examined.) 
            • The compression and decompression takes places while requesting from either of cache levels to its next succeeding level.
	    (preferably from L1 to L2)
      
     
## Algo

The key observation behind BDI compression is that for many cache lines, data values stored in the line have low dynamic ranges. ie.relative differences are small.
In such cases, the line can be represented in a compact form as a common base value plus an array of relative differences called de Deltas.

### BASE-DELTA-IMMEDIATE METHOD:
In this method, input of 256 bits is given to the compressor unit. And outputs like compressed cache line (CCL) and compressible or not
factor (CON) are obtained.

### COMPRESSION:
 • Initially the 32 byte uncompressed Cache line(input UncompCache) is read and stored in input variable. Flag variables (flagX_Y), 
   compressible or not factors (CONX) and delta values (delX_Y) and declared.
 • Flag variable decides whether the delta value obtained is a negative or a positive value and is used to subtract or add to base 
   while decompression.
 • CON is for knowing whether the data is compressible or not. This depends on the logic followed.
 • Delta values are the differences read between base and the next series occurring in the input data.
 • The final compressed cache line is of the form {Base, followed by delta values}

### DECOMPRESSION:
 • Decompression is all about checking the CON condition and then the Flag variable, do the required arithmetic operation and the 
   display.
