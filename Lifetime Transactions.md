= CALCULATE(
	[Total Transactions] , 
		ALLEXCEPT( Sales , Customers[Customer Names] ))
