# Analysis of Stocks

## Overview of Project
#### Purpose

> Our client has asked us to do research on the entire stockmarket database given to us. Our goal is to optimize the code for the previous All Stocks Analysis to run through these thousands (3013) of stocks in a way that is most efficient. As a result, the refactored module should pull the Total Daily Volume and Return for the years 2017 and 2018 faster. 

## Results - Comparing Original with Refactored Code
We had an initial code that ran each output year at the following speeds:

##### > *Initial Code Timer for 2017* (1.234375sec)
![image](https://user-images.githubusercontent.com/103383489/173245610-1fd34fc4-0f8d-4e54-9fdf-d63e0dcdd190.png)

##### > *Initial Code Timer for 2018* (1.210938sec)
![image](https://user-images.githubusercontent.com/103383489/173245703-58c3c37d-708a-4cfb-ad7a-17e98cde1942.png)

### Refactor Steps
The code was examined to refactor where the module could be optimized. Here were the steps taken to refactor. 

1) The ```tickerIndex``` is set equal to zero before looping over the rows.

![image](https://user-images.githubusercontent.com/103383489/173246213-d42daa8a-cf7c-460b-bb27-6ea4425f9f67.png)

2) Arrays are created for `tickers`, `tickerVolumes`, `tickerStartingPrices`, and `tickerEndingPrices`

![image](https://user-images.githubusercontent.com/103383489/173248400-d6b74059-61d9-43aa-b388-cb3043433982.png)

3) The `tickerIndex` is used to access the stock ticker index for the `tickers`, `tickerVolumes`, `tickerStartingPrices`, and `tickerEndingPrices` arrays

![image](https://user-images.githubusercontent.com/103383489/173248605-f609ac6d-891a-485d-bfe4-777fd419f361.png)

4) The script loops through stock data, reading and storing all of the following values from each row: `tickers`, `tickerVolumes`, `tickerStartingPrices`, and `tickerEndingPrices` 


![image](https://user-images.githubusercontent.com/103383489/173248558-9dd69cb1-bbcf-4df3-91f5-4d9fe685fbd6.png)

5) Formatting

![image](https://user-images.githubusercontent.com/103383489/173248758-dcf033f8-4faf-4587-a2e4-66ee4dd09273.png)

##### > *Refactored Code Timer for 2017* (0.1757813sec)

![image](https://user-images.githubusercontent.com/103383489/173249022-b64a27f8-4e8c-4c26-8e17-4d4c4f876ccb.png)

##### > *Refactored Code Timer for 2018* (0.1835938sec)

![image](https://user-images.githubusercontent.com/103383489/173249002-ba36be3c-969f-4779-9d3d-0bb0db945912.png)

### Summary - Pros and Cons of Refactoring

The advantages of refactoring code in general:

  - Can help someone who drops in to take over the project understand the code more quickly. Makes it easier to understand and cuts out excess.
  - Helps the code run faster.
  - Uses less memory.
 
The disadvantages of refactoring code in general:

  - Time taken to rewrite pieces of the over all code. 

The advantages of refactoring the "All Stocks Analysis" code:

  - Cut the time taken to run the code by .75 seconds
  - Sets up a more efficient and easier to understand structure if the code needs to be revisited in the future.

The disadvantages of refactoring the "All Stocks Analysis" code:

  -None, other than the time taken reworking it.
  
 ### Improvement in efficiency and organization are always worth the time, especially if it helps maintain the overall function of the program wanting to be run.
