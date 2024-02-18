= SUMX( Sales,
	Sales[Quantity] * RELATED( Products[Current Price] ) )
