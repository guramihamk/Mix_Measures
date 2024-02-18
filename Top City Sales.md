= CALCULATE ( 
	[Total Sales] , 
		TOPN ( 5 , 
			 Regions , 
				[Total Sales] )
)
