# mmSignature
Data for paper 'mmSignature: Semi-supervised Human Identification Based on Millimeter Wave Radar'
Yicheng Yao, Hao Zhang, Changyu Liu, Fanglin Geng, Peng Wang, Lidong Du, Xianxiang Chen, Baoshi Han and Zhen Fang
E-mail addresses: yaoyicheng19@mails.ucas.ac.cn (Y. Yao)

We conducted four sets of human identification experiments, including 10 monitoring users and 10 other users. For the other users, the model needs to distinguish them from the monitoring users, but it does not need to know who they are. 

# Data Annotation
In each set of experiments, we mark the coordinates of the exclusive location of the monitoring user.  If the user starts from or returns to the marked position, the signal is assigned as the user's label. Otherwise, the data is assigned to the "unknown" label. The data of the monitored user includes both the data of starting or returning to the marked position and the data of moving in other places. Therefore, the data labeled "Unknown" contains both the monitoring user's data and other people's data.

# Data Format
The.npy file records a list of point cloud data, range-velocity map data, and target tracking results. Each file is a list in the format [ [ Point cloud ], [ Target list ], [ Range-Velocity map ], label]. 

In the training set, labels ' 0 ' represent ' Unknown ' samples, and labels ' 1 ', ' 2 ', ' 3 ' represent samples of different monitoring users. In the test set, the label ' 0'represents the sample of other users.

The range-velocity map data format is : [ Frame, Range, Velocity ] 

The format of the point cloud is : [ Frame,1, number of point clouds, [elevation,azimuth,doppler,range, snr] ] 

The format of Target list is :[tid,posX,posY,velX,velY,accX,accY,posZ,velZ,accZ]
 
# Dataset
The data set is published at https://drive.google.com/drive/folders/1rGRe1RbLyo1h_0VrnD-lui0c-qqWVOC9?usp=sharing
