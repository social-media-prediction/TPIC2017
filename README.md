## Temporal Popularity Image Collection (TPIC)
For temporal prediction on popularity, TPIC is an temporal image popularity dataset with 680K photos and corresponding anoynimized photo-sharing records on Flickr ranges of 3 years. Specifically, TPIC is also a multi-faceted data collection, which contains photo image, user profile and photo metadata. We provide the popularity as the normalized views of each photo sharing behaviors. In order to protect the private information of sharing behaviors, we convert the timestamps to segmented time information and indexed of it by integer numbers. To ensure the generalizability of our results, we sampled 100K, 200K and 400K photos with time-order. 
## Download Data
* [user&photo metadata](https://drive.google.com/open?id=0B7yqoohfGsHNZjFPX21sY2h0ZmM) (4.5MB)
* [photo urls](https://drive.google.com/open?id=0B7yqoohfGsHNd2d3eUVjZ1VtOVk)(6MB)
* [time flag](https://drive.google.com/open?id=0B7yqoohfGsHNZnhuMzRfbnpfZHM)(2.5MB)
* [labels](https://drive.google.com/open?id=0B7yqoohfGsHNTUhLWmpxXzc4dGs)(3MB)

## Data Organization
Each row of data has a unique picture id(pid) along with user id(uid). All the CSV files listed above have data header that demonstrate the the meaning of the column.
### USER_META.txt
The file organization inside the file contains picture id, user id, comment count, has people, title length, description length, tag count, average view, group count, average member count information:  

```
pid uid commentcount haspeople titlelen deslen tagcount avgview groupcount avgmembercount  
...  
304582	50@N31	0	0	15	0	14	199.32	1188	6601
304592	142@N94	0	0	11	9	0	615.61	67	21637
... 
```
THe data is crawled from Flickr with user id and photo id anonymized
### PHOTO_URL.txt
Data organized inside the file are the phtoto urls correspond to given photo id and user id:
```
pid uid url
...
9624	25@N92	https://www.flickr.com/photos/7626362@N07/1251837061
665085	275@N38	https://www.flickr.com/photos/7690920@N06/863366976
...
```
### TIME_FLAG.txt
In order to use temporal information from dataset while protecting the user privacy, we extract year, month, day, and hour index with corresponding photo and user from dataset:
```
pid uid year month day hour_index
...
311862	11@N30	2007	3	16	4
311863	89@N59	2007	3	16	4
...
```
The definition of hour index is defined below:
* Hour Index

* 0: 2am-6am

* 1: 6am-10am

* 2: 10am-2pm

* 3: 2pm-6pm

* 4: 6pm-10pm

* 5: 10pm-2am

### LABEL.txt
The label file contains the popularity (log-views), picture id with associate user id:
```
pid uid logview
...
9624	25@N92	3.2
665085	275@N38	2.3
...
```
