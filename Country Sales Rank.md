= IF ( HASONEVALUE( Regions[Country] ),
RANKX ( 
	ALL ( Regions[Country] ) , 
		[Total Sales] , ,
			DESC
), 
BLANK())
