# what an order book is
An order book stores all outstanding bug and sell orders that have not yet been executed or cancelled. Orders 
are organized by price-time priority. Better prices are ranked ahead of worse prices, and orders at the same 
price are processed in FIFO order 

# what operations it supports 
Insert order, cancel order, modify order, match order, display market depth, query best bid, query best ask 

# how matching works 
Whenever the highest bid is greater than or equal to the lowest ask, the matching engine executes trade 
according the price-time priority until no more executable orders remain 

# Price priority 
For buy orders(bids): Higher price means higher priority 
For sell orders(asks): Lower price means higher priority 
This is because buyers wnat to pay as little as possible, while sellers want to sell for as much as possible. 
The matching engine will always ranks bids from highest to lowest, and asks from lowest to highest. 

# Time priority 
If two orders have the same price, the order that arrived first is executed first

# Partial fills
A partial fill occurs when one order's quantity is larger than the matching order 
For example, the bid is 100 shares and ask is 80 shares, 
so the bid order will be partially filled

# What fields should the Order class contains? 
Order ID, Side(Buy / Sell), Price, Original Quantity, Remaining Quantitiy, Timestamp

# Why should Price be a scaled integer instead of double?

Using floating-point types (float/double) to represent prices can introduce precision errors because many decimal values cannot be represented exactly in binary.
The binary floating-point cannot exactly represent many decimal fractions, which can introduce rounding erros during arithmetic and comparisons 

For example:

0.1 + 0.2 != 0.3

These small errors may lead to incorrect price comparisons or unexpected arithmetic results.

Instead, this project stores prices as scaled integers (fixed-point representation).

Example (2 decimal places):

Scale = 100

$10.35
↓

1035

$0.10
↓

10

All arithmetic and comparisons are performed using integers.

The decimal point is only added back when displaying the price to users.

Benefits

- Exact comparisons
- No floating-point rounding errors
- Faster integer arithmetic
- Easier debugging
- Common approach used in many financial and trading systems