= CALCULATE(
	[Total Sales] , 
	VALUES( Products[Product Name] ),
	FILTER(
		CALCULATETABLE(
			ADDCOLUMNS(
				ADDCOLUMNS(
					VALUES( Products[Product Name] ),
					"OuterValue", [Total Sales]
				),
				"CumulatedSalesPercentage" , DIVIDE(
					SUMX(
						FILTER(
							ADDCOLUMNS(
								VALUES( Products[Product Name] ),
								"InnerValue", [Total Sales]
							),
							[InnerValue] >= [OuterValue]
						),
						[InnerValue]
					),
					CALCULATE(
						[Total Sales],
						VALUES( Products[Product Name] )
					)
				)
			),
			ALL( Products )
		),
		[CumulatedSalesPercentage] > [Min Boundary]
		&& [CumulatedSalesPercentage] <= [Max Boundary]
	)
)
