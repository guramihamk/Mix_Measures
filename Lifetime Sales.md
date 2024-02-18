= CALCULATE(
	[Total Sales] , 
		ALLEXCEPT( Sales , Customers[Customer Names] ))
