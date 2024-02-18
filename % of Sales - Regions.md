= DIVIDE ( [Total Sales] , 
	CALCULATE ( [Total Sales] , 
		ALL ( Regions )
	),
0)
