# EPICsoildata
GetImportantSoilDataforEPICsimulation

This code defines a function get_soil_data that takes as input the latitude and longitude of a location. The function uses the get_ssurgo_soil_profile function from the apsimx package to import soil profile data from the SSURGO database for the specified location, including 10 soil layers. The imported data is stored in the variable soil_profile.

Next, the function converts soil_profile to a data frame soil_df using the matrix function and the unlist function to flatten the nested list structure of soil_profile. The resulting data frame contains one row for each soil horizon, with each column representing a soil property. The column names are initially assigned default names (X1, X2, etc.).

The column names are then renamed to more meaningful names using colnames. The function extracts only the columns of interest from soil_df and discards the rest, and returns the resulting data frame.

Finally, the function is called with a specified latitude and longitude, and the resulting data frame is displayed in a View() window.
