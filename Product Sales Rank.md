= IF ( HASONEVALUE( Products[Product Name] ),
RANKX ( 
	ALL ( Products ) , 
		[Total Sales] , ,
			DESC
), 
BLANK())
