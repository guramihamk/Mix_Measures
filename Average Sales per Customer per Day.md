= AVERAGEX (
	VALUES ( Dates[Date] ),
	AVERAGEX( 
		VALUES( Customers[Customer Names] ),
			[Total Sales]
))
