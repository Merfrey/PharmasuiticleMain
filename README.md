# PharmasuiticleMain
Module 5 for data analysis class
Uzuma assisted with lines 6, 7, 13.

6


# Optional: Get all the data for the duplicate mouse ID.
mouse_data_complete["Mouse ID"] == "g989"



7


duplicated_mouse_summary = mouse_data_complete[mouse_data_complete["Mouse ID"] == "g989"]



13



# A more advanced method to generate a summary statistics table of mean, median, variance, standard deviation,
# and SEM of the tumor volume for each regimen (only one method is required in the solution)
mouse_summary_data = mouse_data_complete.groupby("Drug Regimen")["Tumor Volume (mm3)"].agg(["mean", "median", "var", "std", "sem"])
# Using the aggregation method, produce the same summary statistics in a single line
