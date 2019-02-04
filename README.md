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
  
  
