= CALCULATE( 
	[Sales LY] , 
	FILTER(
		ALLSELECTED( Dates ),
		Dates[Date] <= MAX( Dates[Date])
	)
)
