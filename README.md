# mmSignature
We conducted four sets of human identification experiments, including 10 monitoring users and 10 other users. For the other users, the model needs to distinguish them from the monitoring users, but it does not need to know who they are. 

# Data Annotation
In each set of experiments, we mark the coordinates of the exclusive location of the monitoring user.  If the user starts from or returns to the marked position, the signal is assigned as the user's label. Otherwise, the data is assigned to the "unknown" label. The data of the monitored user includes both the data of starting or returning to the marked position and the data of moving in other places. Therefore, the data labeled "Unknown" contains both the monitoring user's data and other people's data.

# Data Format
The.npy file records a list of point cloud data, range-velocity map data, and target tracking results. Each file is a list in the format [ [ Point cloud ], [ Target list ], [ Range-Velocity maps ], label]. 
 
# Dataset
The data set is published at https://drive.google.com/drive/folders/1rGRe1RbLyo1h_0VrnD-lui0c-qqWVOC9?usp=sharing
