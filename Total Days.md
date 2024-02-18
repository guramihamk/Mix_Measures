= IF( HASONEVALUE( 'Date Ranges'[Time Frame] ), VALUES( 'Date Ranges'[Days] ), COUNTROWS( Dates ) )
