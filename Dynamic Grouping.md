= CALCULATE(
	[Total Sales] , 
		FILTER(
			VALUES( Regions[Country] ),
			COUNTROWS(
				FILTER(
					'Price Ranges',
					[Profit Margin] >= 'Price Ranges'[Min]
					&& [Profit Margin] < 'Price Ranges'[Max] 
				)
			) > 0
		)
)
