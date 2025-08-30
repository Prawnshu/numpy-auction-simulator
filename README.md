# numpy-auction-simulator
An ultra-fast, vectorized auction simulator in Python to empirically validate the Revenue Equivalence Theorem.

Revenue equivalence theorem states that under certain conditions, all standard auction models will yield the same expected revenue for the seller.
  Key assumptions made - 
  
    1) Bidders are risk neutral (aka. indifferent to risk), meaning their utility is a linear function of money.
    2) All bidders have the same valuation distribution (symmetry), making them statistically identical in terms of risk and opportunity.
    3) Each bidder’s valuation is independent and known only to them.
    4) The auction allocates the item to the bidder with the highest valuation (allocation efficiency).

This simulator validates the revenue equivalence theorem visually, using first price and second price auctions.

First-price sealed-bid auction, the winning participant is the one who submits the highest bid, and they pay the exact amount of their own winning bid. 

Second-price sealed-bid auction (Vickery auction), the winning participant is still the one who submits the highest bid, but they must pay the amount of the second-highest bid. 

Distribution of seller revenue when visualised over multiple simulations shows that for consistent payouts, they should pick first-price auction.
If the seller has more risk appetite then they should pick second-price auction. However on average, both the types of auctions lead to the same avg revenue for the seller.
