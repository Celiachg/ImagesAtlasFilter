import pandas as pd

# Specify the full path to your Excel file
excel_file_path = 'excel_file_path.xlsx'

# Load the Excel file into a pandas DataFrame
df = pd.read_excel(excel_file_path)

# Calculate the mean of CCFv3 X coordinates of all detections for each image
means = df.groupby('Image')['Atlas_X'].mean()

# Filter the means to keep only those between 10.10 and 10.60 inclusively
filtered_means = means[(means >= 10.10) & (means <= 10.60)]

# Merge the filtered means with the original DataFrame to include the 'Image' column
filtered_means = pd.merge(filtered_means, df[['Image']], on='Image', how='inner').drop_duplicates(subset='Image')

# Path for the output Excel file
output_path = 'output_path.xlsx'

# Save the final data to a new Excel file
filtered_means.to_excel(output_path, index=False)
