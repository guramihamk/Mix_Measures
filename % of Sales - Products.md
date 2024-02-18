= DIVIDE ( [Total Sales] , 
	CALCULATE ( [Total Sales] , 
		ALL ( Products )
	),
0)
