# Project Documentation

## Section 1: Project Purpose and Scope

The purpose of this project is to analyze and visualize fire incident data from the City of Toronto's Open Data Portal. By examining detailed information about fire incidents, including the area of origin,  civilian casualties, and more, the aim is to provide insights that can help improve fire safety measures and resource allocation.

This project involves creating two distinct data visualizations:

Bar Chart: This visualization will showcase the top 10 most frequent areas of origin for fire incidents, highlighting the frequency and associated estimated dollar loss. This information is crucial for identifying high-risk areas and understanding the financial impact of fire incidents.

Heatmap: This visualization will illustrate the relationship between fire incidents and the presence of fire alarm systems. By analyzing civilian casualties in different areas of origin with and without fire alarm systems, we aim to evaluate the effectiveness of fire alarm systems in reducing casualties.

The intended audience for these visualizations includes fire safety analysts, policymakers, emergency response teams, and public health officials. These stakeholders can use the insights from the visualizations to make informed decisions about fire safety strategies and resource allocation.

Overall, this project aims to provide valuable data-driven insights that can contribute to enhancing fire safety and reducing the risk and impact of fire incidents in Toronto.

## Section 2: Data Visualization

The visualizations included are:

- **Bar Chart**: Showing the top 10 most frequent areas of origin for fire incidents.
- **Heatmap**: Illustrating the relationship between fire incidents and the presence of fire alarm systems.

### Bar Chart: "Top 10 Most Frequent Areas of Origin for Fire Incidents"

**Dataset:**

- **Name**: Fire Incidents
- **Source**: [City of Toronto Open Data Portal](https://open.toronto.ca/dataset/fire-incidents/)
- **Description**: This dataset includes only fire incidents as defined by the Ontario Fire Marshal (OFM) up to December 31, 2023. It provides detailed information about fire incidents to which Toronto Fire Service (TFS) responds. The data includes information on the area of origin, building status, business impact, civilian casualties, and other related variables.

**Variables Used:**

- **Area_of_Origin**: The specific area within a property where the fire originated (e.g., Cooking Area or Kitchen, Porch or Balcony).
- **Frequency**: The count of fire incidents that originated from each area.
- **Estimated_Dollar_Loss**: The estimated financial loss caused by the fire incidents, in dollars.
- **Civilian_Casualties**: The number of civilian casualties, including fire-related injuries and fatalities.

**Transformations and Calculations:**

- **Data Cleaning**: Rows with missing values in the 'Area_of_Origin', 'Estimated_Dollar_Loss', and 'Building_Status' columns were dropped.
- **Imputation**: Missing numerical values were filled with the median value of the respective columns. Missing categorical values were filled with the mode.
- **Selection**: The top 10 areas of origin with the highest frequency of fire incidents were selected for the visualization.

**Visualization:**

- **Software Used**: Plotly Express (Python)
- **Purpose**: To highlight the most common areas of origin for fire incidents in Toronto and the associated estimated dollar loss.
- **Design Choices**:
  - **Color Scale**: 'Plasma' color scale based on 'Estimated_Dollar_Loss' to visually differentiate areas with varying financial impacts.
  - **Axes Labels**: Clearly labeled axes for 'Area of Origin' and 'Frequency of Incidents'.
  - **Title**: A descriptive title indicating the focus of the visualization.
  - **Grid Lines**: Light grey grid lines to enhance readability.
  - **Annotations**: Hover data to provide additional information on estimated dollar loss and civilian casualties.

**Analysis of Results:**

The bar chart reveals that the most frequent area of origin for fire incidents is the Cooking Area or Kitchen, with a significantly higher frequency compared to other areas. This is followed by Porch or Balcony and Sleeping Area or Bedroom. The high frequency in kitchens can be attributed to the common use of heat sources and cooking appliances, which are potential ignition sources. The visualization also highlights that the Cooking Area or Kitchen has the highest estimated dollar loss, indicating that fires originating in this area tend to cause substantial financial damage.

### Heatmap: "Fire Incidents by Area of Origin and Fire Alarm System Presence"

**Dataset:**

- **Name**: Fire Incidents
- **Source**: [City of Toronto Open Data Portal](https://open.toronto.ca/dataset/fire-incidents/)
- **Description**: This dataset includes detailed information about fire incidents to which Toronto Fire Service (TFS) responds. It includes data on the area of origin, fire alarm system presence and operation, and the number of civilian casualties.

**Variables Used:**

- **Area_of_Origin**: The specific area within a property where the fire originated.
- **Fire_Alarm_System_Presence**: Indicates whether a fire alarm system was present at the fire origin.
- **Civilian_Casualties**: The number of civilian casualties, including fire-related injuries and fatalities.

**Transformations and Calculations:**

- **Data Cleaning**: Rows with missing values in the 'Area_of_Origin', 'Fire_Alarm_System_Presence', and 'Civilian_Casualties' columns were dropped.
- **Imputation**: Missing values were handled as described for the bar chart.
- **Aggregation**: The data was aggregated to calculate the sum of civilian casualties for each combination of area of origin and fire alarm system presence.

**Visualization:**

- **Software Used**: Tableau
- **Purpose**: To show the relationship between the presence of fire alarm systems and the number of civilian casualties in different areas of origin.
- **Design Choices**:
  - **Color Scale**: 'Orange-Gold' color scale to highlight areas with higher civilian casualties.
  - **Axes Labels**: Clearly labeled axes for 'Area of Origin' and 'Fire Alarm System Presence'.
  - **Title**: A descriptive title indicating the focus of the visualization.
  - **Annotations**: Tooltips to provide additional information on the number of civilian casualties for each area and fire alarm system presence status.

**Analysis of Results:**

The heatmap shows that areas like Cooking Area or Kitchen and Sleeping Area or Bedroom have higher numbers of civilian casualties. It also reveals that the presence of fire alarm systems does not consistently correlate with lower casualty numbers in all areas. For instance, despite the presence of fire alarm systems, the number of civilian casualties remains high in some areas like Cooking Area or Kitchen. This suggests that while fire alarm systems are crucial for early detection and evacuation, they alone may not be sufficient to prevent casualties.




