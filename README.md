# RESTful API's using Flask

## This is a simple application that allows you to view & add items to your transaction history. Provides 4 end points

## View INCOME transactions

`curl http://localhost:5000/incomes`

[
  {
    "amount": 5000.0, 
    "created_at": "2017-11-19T16:08:21.332346", 
    "description": "Salary", 
    "type": "TransactionType.INCOME"
  }, 
  {
    "amount": 200.0, 
    "created_at": "2017-11-19T16:08:21.332352", 
    "description": "Dividends", 
    "type": "TransactionType.INCOME"
  }
]

## 2) View EXPENSE transactions

[
  {
    "amount": -50.0, 
    "created_at": "2017-11-19T16:08:21.332355", 
    "description": "pizza", 
    "type": "TransactionType.EXPENSE"
  }, 
  {
    "amount": -100.0, 
    "created_at": "2017-11-19T16:08:21.332356", 
    "description": "Show", 
    "type": "TransactionType.EXPENSE"
  }
]


`curl http://localhost:5000/expenses`

## 3) Add a new INCOME transaction

`curl -X POST -H "Content-Type: application/json" -d '{"amount": 100, "description": "loan payment"}' http://localhost:5000/incomes
`
## 4) Add a new EXPENSE transaction

`curl -X POST -H "Content-Type: application/json" -d '{"amount": 2000, "description": "tuition"}' http://localhost:5000/expenses
`