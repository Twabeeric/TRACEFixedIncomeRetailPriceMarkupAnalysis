# TRACE-Fixed-Income-Retail-Price-Markup-Analysis
Our model utilized a big data approach to attempt to understand and pin down average markups in the industry
## Context
The fixed income market in the United States is a notoriously opaque market
As a result, it is very difficult, if not impossible, to track and quantify the markups that are being charged 
## Securities Presented
The scope of our research focused on Corporate, Municipal, and MBS. Based on the current holdings of Detalus, this analysis would provide the best ballance of potential insight and large computationally heavy computer modeling.

## Securities Ignored
TBA, ABS, and CMO securities will not be presented in this report. The analysis is only as good as the raw data. These files did not include information on interdealer interaction and thus made it impossible to develop meaningful insight.

## Limitations
The greatest limitation of this project is the anonymity of the data. In every methodology we developed, the crucial step was matching the different sides of each trade. In most cases, the information was not sufficient to execute this process. Thus, the resulting methods either rely on sampling or approximation to estimate true markups. In order to produce reputable results, we made conservative assumptions that produced smaller mark ups than expected. 
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture7.png">

## Research methods
1.Agency Trades
2.Inter-Dealer Pricing
  -20% most Liquid
  -20% least Liquid
  -Single Cusips 
  -Daily lowest interdealer price as cost price
  -Daily volume-weighted interdealer price as cost price

## Methodology: Agency Trades
We consider agency trades to be trades executed as agent and falling within the same date and time.
We filtered our data to match trades that were executed on the same bond, same date, same time, same volume but with different sides i.e. a buy must match to a sell.
We then calculated the markup.
For a dealer sell, we assumed the markup is the difference between the higher customer price minus the lower dealer price divided by the customer price. 
For a dealer buy, we assumed the markup is the difference between the higher dealer price and the lower customer price divided by the customer price. 
Pros: easy to identify trades and markups
Cons: low markups and negative markups

## Methodology: Interdealer Trades
We consider interdealer trades to be trades executed between two dealers.
We filtered our data to produce a table of interdealer trades, they are all coded as sells as only one pair of dealers are required to report the trade.
We found them matched the interdealer trades to other trades executed for the same cusip, on the same day and the same volume.
Pros: identify true cost priceCons: don’t see other side of trades; hedging


We identify the bonds’ trading  liquidity by the product of trading  volume times the trading frequency. 

20% Most Liquid Bonds
Pros: the most traded bonds have a lot of data 
Cons: low markups since these bonds are to liquid.

20% Least Liquid Bonds
Pros: high markups since these bonds are not liquid
Cons: the least traded bonds only have limited data

Single Bond
Pros: find the exact markup of a targeted bond
Cons: a single bond is not general

## Summary Of Results
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture9.png">
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture10.png">
## Corporates: Summary Statistics 2018
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture11.png">
## Corporates: Agent Trades 
These are executed by the dealer on behalf of the client. They are reported on the same date, same time with same volume
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture12.png">
## Corporates: Interdealer Price as Cost Price
The lowest interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture13.png">
## Corporates: VWAP Interdealer Price as Cost Price
The volume-weighted interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price.
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture14.png">
## Municipals: Summary statistics 2018
Municipal bonds were the second largest data set we analyzed. Similar to MBS’s that we will see later, the average markup is larger than corporate bonds but a discount to what is seen in the market. 
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture15.png">
## Municipals: Agent Trades
These are executed by the dealer on behalf of the client. They are reported on the same date, same time with same volume
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture16.png">
## Municipals: Agent Trades
These are executed by the dealer on behalf of the client. They are reported on the same date, same time with same volume
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture17.png">
## Municipals: Interdealer Price as Cost Price
The lowest interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture18.png">
## Municipals: Interdealer Price as Cost Price
The lowest interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture19.png">
## Municipals: VWAP Interdealer Price as Cost Price
The volume-weighted interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price.
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture20.png">
## MBSs: Summary statistics 2018
The final asset class we analyzed was Mortgage Backed Securities. While tarded significantly less frequently than corporate or municipal bonds, the results trended in a very similar area as municipal's.
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture21.png">
## MBSs: Agent Trades
These are executed by the dealer on behalf of the client. They are reported on the same date, same time with same volume
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture22.png">
## MBSs: Agent Trades
These are executed by the dealer on behalf of the client. They are reported on the same date, same time with same volume
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture23.png">
## MBSs: Interdealer Price as Cost Price
The lowest interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price.
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture24.png">
## MBSs: VWAP Interdealer Price as Cost Price
The volume-weighted interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price.
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture25.png">
## MBSs: VWAP Interdealer Price as Cost Price
The volume-weighted interdealer price executed for each cusip on each day is taken as the cost price and other retail trades marked off this price.
<img width="800" src="https://github.com/Twabeeric/TRACE-Fixed-Income-Retail-Price-Markup-Analysis/blob/master/Picture26.png">

