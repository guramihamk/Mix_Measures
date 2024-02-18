= CALCULATE( [Revenue],
	FILTER( Dates,
		Dates[Date] <= TODAY() && Dates[Date] >= TODAY() - [Total Days]))
