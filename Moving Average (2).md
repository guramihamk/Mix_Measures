= AVERAGEX(
	FILTER(
		ALL( Dates[Date] ),
		Dates[Date] > ( MAX( Dates[Date] ) - 7 ) 
			&& Dates[Date] <= MAX( Dates[Date] )
	),
	[Total Sales]
)
