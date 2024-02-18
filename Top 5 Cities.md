= IF( HASONEVALUE( Regions[City]) ,
	IF ( 
	[Regional Sales Rank] <= 5 ,
		[Total Sales] , 
			BLANK()
	)
)
