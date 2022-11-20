# Variable Rate Swap Valuation

Variable rate swap is a special type of interest rate swap in which one leg of the swap corresponds to fixed rate payments while the other involves fixed rate payments for an initial period of time and a floating rate for the rest. The floating rate on that portion is defined as a minimum of two index rates.

The fixed rate leg is similar to a fixed rate bond. The bond price is computed by discounting each coupon descripted at https://finpricing.com/lib/FiBond.html

	We treat the two index rates as assets whose values are lognormally distributed random variable. Their pricing procedure uses discount factors retrieved from the EURIBOR curve.
	
	The present value of the minimum of two assets, s1 and s2, is given by the formula
	
	 		(1)
	
	where
	
•	 ,
•	1 and 2 are the volatilities of s1 and s2 respectively,
•	 is the correlation of the two risk factors,
•	T is the maturity time,
•	  and  are the expected values of s1 and s2 at maturity (future values),
•	D(T) is the discount factor implied by the yield curve.

It is forward two index rates as retrieved from the yield curves that should be used for   and  .
The minimum of two values, s1 and s2, can be expressed as 

p = min(s1,s2) = s1 – max(s1-s2, 0)				(2)

If s1 and s2 are two risky assets, the present value of p at some future time T is 

 					(3)

where P(0,T) is the discount factor implied by the yield curve. Assuming the asset values lognormally distributed, the expectation of max(s1-s2, 0) at maturity can be found as the value of the so called “Exchange-One-Asset-for-Another” European option [2,3] and is given by the following equation:

	 			(4)

where

•	 
•	1 and 2 are the volatilities of s1 and s2 respectively,
•	 is the correlation of the two risk factors
•	T is the maturity time
•	  and  are the expected values of s1 and s2 at maturity (future values).

Combined, Eqs. (2), (3) and (4) yield

 	 		(5)


