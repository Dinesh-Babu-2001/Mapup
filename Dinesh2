import pandas as pd

def get_type_count(df):
  """
  This function takes a DataFrame and adds a new categorical column based on the values of the 'car' column.
  It then calculates the count of occurrences for each category and returns the result as a dictionary.

  Args:
    df: A DataFrame with a column named 'car'.

  Returns:
    A dictionary containing the count of occurrences for each category.
  """
  # Add a new categorical column based on the values of the 'car' column
  df['car_type'] = pd.cut(df['car'], bins=[0, 15, 25, float('inf')], labels=['low', 'medium', 'high'])

  # Calculate the count of occurrences for each category
  type_counts = df['car_type'].value_counts().to_dict()

  # Sort the dictionary alphabetically based on keys
  sorted_type_counts = dict(sorted(type_counts.items()))

  return sorted_type_counts

# Example usage
df = pd.DataFrame({
  'id_1': [1, 2, 3, 4, 5],
  'id_2': [2, 3, 4, 5, 1],
  'route': [10, 20, 30, 40, 50],
  'moto': [1, 2, 3, 4, 5],
  'car': [10, 20, 30, 40, 50],
  'rv': [1, 2, 3, 4, 5],
  'bus': [1, 2, 3, 4, 5],
  'truck': [1, 2, 3, 4, 5]
})

type_counts = get_type_count(df.copy())

print(type_counts)
