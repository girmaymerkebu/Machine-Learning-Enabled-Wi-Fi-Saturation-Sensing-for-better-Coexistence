# Dataset Description
In order to develop a CNN model that can classify saturated and unsaturated traffic in WiFi network, we prepared a large dataset that represents the traffic characteristics of both cases.  In this dataset collection, different scenarios of saturated and unsaturated 802.11a network are modelled in ns-3. 
Different saturated and unsaturated network scenarios were generated by varying the packet arrival rate (PAR) and number of active nodes. 
The PAR is tuned below and above a grey region of saturation point for saturated and unsaturated networks respectively. 
Once the PAR of saturation point for a specific network configuration is determined to be PARsat, the grey region is defined when 
the PAR lies between PARsat − 250packet/s and PARsat + 250packet/s. UDP traffic was generated at different packet arrival rates to investigate 
the traffic characteristics of different load levels covering a wide range of performance variations in saturated and unsaturated traffic cases. 
For each configuration and traffic load examined in this study, the simulation run-time was set to 20 minutes. Then, the starting time and duration of each frame 
accessing the medium is monitored to generate the IFS distribution and collision percentage. This channel monitoring is done based on frames transmitted 
after the first minute, as the 802.11 association process takes place in the start up of the connection between the AP and the stations.
Each element E in a row of the dataset is obtained by monitoring IFS and percentage of collision and is composed of (x1, x2, ..., x26, y1, y2, ..., y26, s, r, l). 
The values fx1, x2..., x26, y1, y2, ..., y26 represent the histogram of the IFS values for the M frames that accessed the medium in 60 seconds duration. 
x26 represents the maximum IFS duration (in ms) in the considered M frames whereas x1 is x26/26. The remaining xi values are buckets at uniform spacing between x1 and x26. 
![image](https://user-images.githubusercontent.com/51439390/167096857-e1b65577-8a39-4597-8630-bd614de30d35.png)

For i>1, the values of yi represent the IFS histogram count (in percentage) for a corresponding bucket interval between xi-1 and xi. 
In the case of y1, the bucket interval is between 0 and x1. The s and r in the sequence of the dataset element represent the average IFS duration (in ms) and percentage of frame collisions respectively. The average IFS duration is computed by averaging the IFS between each frame in the dataset element over the total number of frames.
Similarly, the collision percentage is computed by counting the frames that are not acknowledged (if no corresponding ACK frame is received by the transmitter). 
The last parameter in the data set element is l which represents the labeling. Labels "1" and "0" represent saturated and unsaturated Wi-Fi networks respectively. 
Based on this approach, 20,000 sample elements are collected with a more or less equal portion of saturated and unsaturated traffic scenarios.



# References
[1] M. Girmay, A. Shahid, V. Maglogiannis, D. Naudts and I. Moerman, "Machine Learning Enabled Wi-Fi Saturation Sensing for Fair Coexistence in Unlicensed Spectrum," in IEEE Access, vol. 9, pp. 42959-42974, 2021, doi: 10.1109/ACCESS.2021.3066052.
