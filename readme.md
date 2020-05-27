# Takehome Exercise 

A large bank Oldman Socks has hired you to help develop a new loan product to provide a line of credit to business customers. At the heart of this product is an accounting system to used by other product engineerings at Oldman. You have been tasked with developing this system.

The system needs to track events and balances for a number of different ledger types for each customer. For example, a set of ledger types might include: `principal`, `application_fee`, `principle_paid`, `interest_fee` , `interest_fee_paid` and `late_fees`. During the relationship of the customer with Oldman Socks the system will process different events, each changing the  balances of one or more ledger types. The system need to be able to process the events and keep track of all balances for any given date. The ledger types tracked by the product might be expanded in the future.

For example a series of events for a particular customer might look like this: 

- a customer takes out a loan on 1/1/2020, with `principal` amount of $1000, and an `application_fee` amount of $10.
- On 2/1/2020  an `interest_fee` amount of $5 is added.
- On 3/1/2020, the customer makes a payment of $100 and as a result, the `interest_fee` is reduced to $0 and `principal` goes down by $95 to a balance of $905. A `principle_paid` ledger type is added with a value of $95 and an `interest_fee_paid` ledger type is added with a value of $5.
- On 4/1/2020 the `interest_fee` amount again goes up by $5.
- On 4/5/2020 the bank decides that the customer is late on their monthly payment and add $40 to a new ledger type `late_fees`.

In addition to processing events for different ledger types, the system should allow other product engineers to do the following: 

- Provide the most recent balance of all the available ledger types.
- Provide the balance of a specific ledger type on a specific date in the past.
- Provide the previous balance of a specific ledger type (that differs from the current balance of that ledger type)

Implement this data structure in a language of your choice. Note that you do not have to figure out how much principle or fees to charge - just a data structure interface for other engineers to program in the business logic. When you are done, you can push the code to a git repository or just send over a zip file.
