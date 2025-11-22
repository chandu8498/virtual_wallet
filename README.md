Data Model:
  Customer Details: CustId, Customer Name, MobileNo, Email, AccountNo, IFSC Code, Wallet Balance
  Product Details : product_Id, Product_Name, prdCost, merchant_id
  Merchant Details : Merchant_id, merchant_name,mobile, email, currency, merchant accountno ,ifsc code:
  Transaction Details: User_Id, Merchant_Id, amount, txn+status, txn_date.
  Wallet_Details :  cust_Id, walletId, credited date, debited date, available bal, currency.
  


API Contracts:
 Create Customer : http://localhost:8080/createCustomer --> @RequestBody -->Customer Name, MobileNo, Email,       AccountNo,  IFSC  Code, Wallet Balance:
 Get Customer : http://localhost:8080/{custId}/getCustomerDetails
                               ResponseEntity<CustomerDetails>  
 CheckBalance :  GET --> http://localhost:8080/{custId}/checkBalance -->
                               ResponseEntity<walletDto> --> currency, avlbal:
 updateBalance : PUT --> http://localhost:8080/addBalance -->
                               RequestBody --> custId,currency,amoutToBeAdded
                               ResponseEntity<walletdto> --> currency, avlBal:   

 Initiate Payment: POST --> http:localhost:8080/initiatePayment 
                            RequestBody   --> custId,Prod_Id,amount,currency, merchant accnt_No.
                            ResponseEntity<txnId, txnStatus>





 
 
