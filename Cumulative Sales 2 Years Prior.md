= CALCULATE( 
	[Sales 2 Yrs Prior] , 
	FILTER(
		ALLSELECTED( Dates ),
		Dates[Date] <= MAX( Dates[Date])
	)
)
