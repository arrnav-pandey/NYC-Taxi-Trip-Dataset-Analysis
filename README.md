# NYC-Taxi-Trip-Dataset-Analysis

## Data Manipulation and Understanding

### Data Types

1. Converted pickup and dropoff to datetime objects for better manipulation.

2. Coordinates are in the float format.

3. Converted vendor_id and trip_duration of integer formats

### Observations

1. We can see there are no missing values in any column present.

2. Some interesting observations can be seen in the passenger count with **min** being 0 and **max** being 9 passengers in one taxi which seems to be odd.

3. Similar that longest trip recorded was 3526282 seconds which comes out to be aroun 40 days?? While the minimum being 1s?

4. The longitude/latitude columns seem to have interesting trends and their density can be analyzed by plotting these trends.

5. The pickup and drop times can give us good insights about the rush hours and peak traffic time.

## Data Visualization and Analysis

### Histogram

![image-20240514003401996](/home/crrankyy/.config/Typora/typora-user-images/image-20240514003401996.png)

Histograms directly show the frequency (or count) of trips falling within specific time intervals (e.g., hourly bins). This allows you to quickly identify peak hours, off-peak hours, and overall patterns in trip demand throughout the day. Time of day is a continuous variable. Histograms are specifically designed for continuous data, allowing you to divide the 24-hour period into bins and see how many trips fall into each bin. From the plot we can infer that the majority of trips commence between 6 PM and 9 PM in the evenings. This aligns well with typical office hours.

### Hexbin Plot

![image-20240514003148328](/home/crrankyy/.config/Typora/typora-user-images/image-20240514003148328.png)

NYC taxi pickup data is often dense, with many pickups occurring in close proximity, especially in busy areas. Hexbin plots effectively visualize this density by aggregating pickup points into hexagonal bins and coloring each bin based on the number of pickups within it. This provides a clear visual representation of pickup hotspots as can be seen in the above plot.

### Scatter Plot

![image-20240514004534459](/home/crrankyy/.config/Typora/typora-user-images/image-20240514004534459.png)

While hexbin plots excel at showing density, scatter plots of pickup and dropoff locations in NYC offers unique advantage in that each point on a scatter plot represents a single taxi trip, with its pickup and dropoff locations plotted as separate points. This allows for a granular view of individual trips, showing the specific origin and destination of each journey. This scatter plot visualizes the overlap between pickup and dropoff coordinates in NYC for a randomly sampled set of 50,000 rides. By using this interactive map, we can easily identify areas where pickups and dropoffs frequently coincide. This allows us to visually assess the degree of overlap between the two sets of coordinates.