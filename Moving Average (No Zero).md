= CALCULATE (
	IF (
		COUNT( Dates[Date] ) >= 7,
		[Total Sales] / CALCULATE( COUNT ( Dates[Date] ) , Sales )
	),
	FILTER (
		ALL ( Dates[Date] ),
		Dates[Date] > (MAX ( Dates[Date] ) - 7 )
			&& Dates[Date] <= MAX ( Dates[Date] )
	)
)
