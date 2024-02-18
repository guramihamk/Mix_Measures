= SUMX( Sales,
	Sales[Quantity] * RELATED( Products[Cost] ) )
