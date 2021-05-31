# Pricing Bond Future Option

A bond future option is an option contract that gives the holder the right but not the obligation to buy or sell a bond future at a predetermined price. The writer/seller receives a premium from the buyer for undertaking this obligation. Options are leveraged instruments that allow the owner to control a large amount of the underlying asset with a smaller amount of money. Bond future options offer significant advantages for reducing costs, enhancing returns and managing risk. They could be European style or American style. 

Bond futures options are also exchange traded derivatives on treasury instruments. They provide market participants with the ability to adjust their interest rate exposures. A bond future option is also a good tool for hedging, income enhancement, duration adjustments, interest rate speculation and spread trading. 

There are established global markets for bond futures and future options so they are very liquid. Investors use bond future options to hedge an existing bond portfolio against adverse interest rate movements or enhance the long-term performance of a portfolio of assets. Arbitrageurs profit from the price difference between the spot bonds and the bond futures. Speculators use bond future option in the hope of making a profit on short-term movements in prices. This presentation provides an overview of bond future option product and valuation. 


	Bond Future Option Introduction
	A bond future option is an option contract that gives the holder the right but not the obligation to buy or sell a bond future at a predetermined price. 
	The writer/seller receives a premium from the buyer for undertaking this obligation.
	Options are leveraged instruments that allow the owner to control a large amount of the underlying asset with a smaller amount of money.
	Bond future options offer significant advantages for reducing costs, enhancing returns and managing risk, as strategic financial instruments.
	A bond future is a future contract in which the asset for delivery is a government bond.
	Bond future options could be European style or American style.



	The Use of Bond Future Options

	Bond futures options are also exchange traded derivatives on treasury instruments. 
	Bond future options provide market participants with the ability to adjust their interest rate exposures.
	A bond future option is also a good tool for hedging, income enhancement, duration adjustments, interest rate speculation and spread trading.
	Bond future options are also liquid. There are established global markets for bond future options.
	Investors use bond future options to hedge an existing bond portfolio against adverse interest rate movements or enhance the long-term performance of a portfolio of assets.
	Arbitrageurs profit from the price difference between the spot bonds and the bond futures.
	Speculators use bond future option in the hope of making a profit on short-term movements in prices. 




	Valuation: European Option


	The present value of a call bond future option is represented as: 



PV(t)=N[F_T Φ(d_1 )-KΦ(d_2)] D_T

where 
d_1,2=[ln(F_T⁄K)±(σ^2 T)⁄2]⁄(σ√T)
K	the strike
	N	the notional
F_T=[(P-C_Σ )  exp⁡(r_T T)-A ]/CF  	the forward clean price of the 
delivered bond (CTD) at t
T	the option maturity date
D_T	the discount factor
   	the conversion factor for a bond to deliver in a bond futures contract
	C_Σ=∑_(t_i≤T)▒〖Cexp(-r_i t_i)〗	the present value sum of all coupons of the 
underlying bond between t and T
	A	the accrual interest before T.
P	the bond dirty price at t
	r_T	the continuously compounded interest rate between t and T
	σ=αDyσ_y/CF	the volatility of forward bond price.
	 	forward yield volatility of the CTD bond of the underlying futures. We use 
the swaption volatility
	 	implied volatility scaling factor
	y	the forward yield that can be solved by P-C_Σ=∑_(T≤t_i≤T_B)▒〖Ce^(-yt_i ) 〗
	T_B	the maturity of the underlying CTD bond
D=(∑_(T≤t_i≤T_B)▒〖t_i Ce^(-yt_i ) 〗)/(∑_(T≤t_i≤T_B)▒〖Ce^(-yt_i ) 〗) 	the forward modified duration of the CTD bond of the 
underlying futures 


	The present value of a put bond future option is represented as: 


PV(0)=N[KΦ(-d_2 )-F_T Φ(〖-d〗_1 )] D_T    


	Valuation:	American Style
	We use the Cox-Ross-Rubinstein (CRR) binomial tree to price American bond future option.
	Build forward bond price tree. 



F_0=[(P-C_Σ )  exp⁡(r_T T)-A ]/CF  
∆t=T/m
F_j^u=F_j e^(σ√∆t) with probability p=(1-e^(-σ√∆t))/(e^(σ√∆t)-e^(-σ√∆t) )
F_j^u=F_j e^(-σ√∆t) with probability 1-p
J = 1,…,m
	σ=αDyσ_y/CF is the volatility described above


	After constructing the tree, valuation is performed backward until the valuation. The option value at node 0 is the present value of the bond future option.



	Practical Guide
	First compute the CTD forward bond price first.
	Then determine the volatility of the forward bond price.
	After that, call Black formula for pricing European bond future options.
	Or build binomial tree to value American bond future options.


	A Real World Example


Option Specification	Future Specification
Buy Sell	Buy	Contract Size	33333.33
Call Put	Call	Conversion Factor	0.8851
Currency	USD	First Delivery Date	6/1/2017
Option Maturity Date	5/26/2017	Last Delivery Date	6/30/2017
Option Expiry Date	5/26/2017	Future Ticker	USM17
Strike	151	Future Ticker Size	32
Option Ticker	USM17C 151	Future Ticker Value	31.25
Settlement Amount	-173875	Number of Contract	52
Settlement Date	2/9/2017	Quote Price	3.34375
		Trade Date	2/9/2017
		Future Maturity Date	6/21/2017
		Underlying Bond Type	UST
		Underlying Bond Coupon	0.05
		Underlying Bond Maturity Date	5/15/2037



References:

https://finpricing.com/lib/EqWarrant.html

https://bitbucket.org/cmrm11/fibondfutureoption/downloads/FiBondFutureOption-12.pdf


