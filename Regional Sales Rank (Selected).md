= IF ( HASONEVALUE( Regions[City] ),
RANKX ( 
	ALLSELECTED( Regions ) , 
		[Total Sales] , ,
			DESC
), 
BLANK())
