The **[[range()]]** function uses a set of indices that point to integer values, which start at the number 0. The numeric values 0, 1, 2, 3, 4 correlate to ordinal index positions 1st, 2nd, 3rd, 4th, 5th. So, when a range call to the 5th index position is made using **range(5)** the index is pointing to the numeric value of 4.

|Index Number|1st index|2nd index|3rd index|4th index|5th index|
|---|---|---|---|---|---|
|Value|0|1|2|3|4|

The **[[range()]]** function can take up to three parameters:  **range(start, stop, step)** 

- **[[range()]] Function Parameters** - Know the roles of the three possible **range(x, y, z)** function parameters:
    - **x** Start of Range (included)
    - **y** End of Range (excluded index) 
        - To include the end of range index, use the expression **y+1**
        - The end of range must be included in the **range()** parameters.
    - **z** Incremental value
    - **Example 1:** range(4, 12**+1**, **2**)
        - This example creates a range that starts at 4 and ends at 12 (without the **+1**, the range would end at 11). 
        - The third parameter increments the range iteration by 2, as opposed to the default increment of 1. The  **range(4, 12+1, 2)** expression would produce the values: 4, 6, 8, 10, 12 
    - **Example 2:** range(10, 2**-1**, **-2**)
        - This example creates a range that starts at 10 and ends at 2**-1**, with a decremental value of **-2**. When counting down, to include the value of the end of the range index, use **-1** (end of range minus 1). This range produces the sequence: 10, 8, 6, 4, 2 