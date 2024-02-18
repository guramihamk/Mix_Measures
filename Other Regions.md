= CALCULATE ( 
	[Total Sales] , 
		FILTER ( Regions , 
			RANKX ( ALL ( Regions ) , [Total Sales] ) > 5 )
)
