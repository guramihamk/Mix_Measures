= IF ( HASONEVALUE( Regions[City] ),
RANKX ( 
	ALL ( Regions ) , 
		[Total Sales] , ,
			DESC
), 
BLANK())
