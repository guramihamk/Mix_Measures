= IF ( HASONEVALUE( Regions[Country] ),
RANKX ( 
	ALL ( Regions[City] ) , 
		[Total Sales] , ,
			DESC
), 
BLANK())
