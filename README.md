# invoice_api


1.   /send_funds                 

Input: 
{
    'amount' :  ,
    'wallet_id ': ,
}

Output: 
{
          'log': 'Funds transferred successfully',
          'flag': constants.responseFlags.ACTION_COMPLETE ,
          'result': result
}


2.  /create_invoice


// generates invoice and inserts it into invoice_tb 


Input: 
{
   'amount' :  ,
   'wallet_id' : ,
}

Output: 

{  
        'log': 'Invoice generated Successfully',
        'flag': constants.responseFlags.ACTION_COMPLETE ,
        'result': response.payment_request 
 }
 
 3. /spend_invoice 
 
 // Decodes the invoice provided, and checks the balance of given wallet is >= to invoice value
 // Checks for in wallet invoices 
 // if the invoice is not in wallet, checks for the 
 
 Input: 
 
 {
   'wallet_id' :   ,
   'invoice' :  
 }
  
  Output: 
  {
       'log': 'Invoice Spent Successfully'
       'flag': constants.responseFlags.ACTION_COMPLETE,
       'result': data
  }
  
  
  4. /send_coins
  
  Input: 
  {
      asset_id :  ' ' ,
      transaction_hash :  ' ',
      address : ' ' ,
      amount : ' ' ,
      lnd : ' '        // for lightning transaction send lnd == 1
  }
  
  Output :  
  {
          'log': 'Funds transferred successfully',
          'flag': constants.responseFlags.ACTION_COMPLETE ,
          'result': result
  }
