# shapes_6dof
The original shapes_6dof dataset is proposed in [1]. based on data provided in [1], For the application of multi-object tracking, we have conducted semi-automatic annotation for each frame the dataset, which users can find under the directory 'images' and its subdirectories. We have also generated ground truth files in a format similar to the MOTChallenge: 'gt.txt', to facilitate the calculation of tracking accuracy. The 'event.txt' file is the event list file, where each line represents an event, denoted as "timestamp (in seconds) x y p", and the 'frame.txt' file specifies the start time for each frame of the image. 
[1] E. Mueggler, H. Rebecq, G. Gallego, T. Delbruck, and D. Scaramuzza,“The event-camera dataset and simulator: Event-based data for pose
estimation, visual odometry, and slam,” The International Journal of Robotics Research, vol. 36, no. 2, pp. 142–149, 2017.

# bmmot_pedestrians/bmmot_vehicles
This dataset was collected by the CeleX5 camera[2], with a resolution of 1280*800. The camera reads events using a row-by-row scanning method. We used the off-pixel mode because other modes have excessively long scanning times (even exceeding 4ms), making them impractical for applications in algorithms that process events one by one. The off-pixel mode can complete a scan of the entire array within typically 10-100 microseconds (related to the event rate）, making it the only viable option. In this mode, the output events do not include polarity information. The file "pedestrians/vehicles.csv" is the raw data, with each row representing an event in the format "y x timestamp (in microseconds)". Since the CeleX5 cannot simultaneously capture grayscale images and events, we had to complete the annotation of the Ground Truth on the binary image accumulated from the events. The raw data is slightly longer than the range of the dataset, we have extracted the first ten seconds of the captured data. It should also be noted that the default coordinate origin of the CeleX5 is at the bottom left, not the top left as commonly used. To maintain consistency with other datasets, we have chosen the top left as the origin. Therefore, the images that users see are inverted vertically.

For the application of multi-object tracking, we have conducted semi-automatic annotation for each frame the dataset, which users can find under the directory 'images' and its subdirectories. We have also generated ground truth files in a format similar to the MOTChallenge: 'gt.txt', to facilitate the calculation of tracking accuracy. The 'event.txt' file is the event list file, where each line represents an event, denoted as "timestamp (in seconds) x y p(1)", and the 'frame.txt' file specifies the start time for each frame of the image. 

[2] CelePixel SDK Reference, CelePixel Technology Co. Ltd., December 2019, document includes detailed API reference and version control
information for CeleX-5 chipset. URL=https://github.com/CelePixel/CeleX5-MIPI

Translation: Some large files have been compressed to meet the file size limit for pushing.




