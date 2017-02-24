## Temporal Popularity Image Collection (TPIC)
TPIC is an image popularity dataset with multi-faceted information, such as user profile, photo metadata, and visual content. It includes 68k user album images with user meta information from over 10 years time-line. Also, we provide normalized label for the convenience to improve data integrity.  It contains 680K photos in total over three years from Flickr. In order to use the temporal information from the dataset, we extracted time information from the metadata. To ensure the generalizability of our results, we sampled 100K, 200K and 400K photos with time-order. 

## Data organization
### USER_META.txt
user meta is contained in the database file.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-9hbo{font-weight:bold;vertical-align:top}
.tg .tg-yw4l{vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 363px">
<colgroup>
<col style="width: 120px">
<col style="width: 243px">
</colgroup>
  <tr>
    <th class="tg-9hbo">Field</th>
    <th class="tg-9hbo">Description</th>
  </tr>
  <tr>
    <td class="tg-yw4l">id</td>
    <td class="tg-yw4l">ID</td>
  </tr>
  <tr>
    <td class="tg-yw4l">pid</td>
    <td class="tg-yw4l">image id</td>
  </tr>
  <tr>
    <td class="tg-yw4l">uid</td>
    <td class="tg-yw4l">user id</td>
  </tr>
  <tr>
    <td class="tg-yw4l">views</td>
    <td class="tg-yw4l">view count</td>
  </tr>
  <tr>
    <td class="tg-yw4l">commentcount</td>
    <td class="tg-yw4l">comment count</td>
  </tr>
  <tr>
    <td class="tg-yw4l">haspeople</td>
    <td class="tg-yw4l">a boolean value 0 or 1</td>
  </tr>
  <tr>
    <td class="tg-yw4l">titlelen</td>
    <td class="tg-yw4l">post title length</td>
  </tr>
  <tr>
    <td class="tg-yw4l">deslen</td>
    <td class="tg-yw4l">post description length</td>
  </tr>
  <tr>
    <td class="tg-yw4l">tagcount</td>
    <td class="tg-yw4l">tag count</td>
  </tr>
  <tr>
    <td class="tg-yw4l">avgview</td>
    <td class="tg-yw4l">average view</td>
  </tr>
  <tr>
    <td class="tg-yw4l">groupcount</td>
    <td class="tg-yw4l">group count</td>
  </tr>
  <tr>
    <td class="tg-yw4l">avgmembercount</td>
    <td class="tg-yw4l">average member count</td>
  </tr>
  <tr>
    <td class="tg-yw4l">year</td>
    <td class="tg-yw4l">year flag</td>
  </tr>
  <tr>
    <td class="tg-yw4l">month</td>
    <td class="tg-yw4l">month flag</td>
  </tr>
  <tr>
    <td class="tg-yw4l">day</td>
    <td class="tg-yw4l">day flag</td>
  </tr>
  <tr>
    <td class="tg-yw4l">hour_index</td>
    <td class="tg-yw4l">hour flag</td>
  </tr>
  <tr>
    <td class="tg-yw4l">url</td>
    <td class="tg-yw4l">image gallery url</td>
  </tr>
</table>


### Photos
Photos Url are contained in the database file as show above

### Hour Index
0: 2am-6am

1: 6am-10am

2: 10am-2pm

3: 2pm-6pm

4: 6pm-10pm

5: 10pm-2am

### TimeFlag.txt
Actually, Time flags are contained in database file. However, we extract it as csv file in case of independent usage.
[Time Flag Download Link](https://drive.google.com/open?id=0B7yqoohfGsHNQVRKQlJHYzZTZ2c)

format:
`id,year,month,day,hour_index`
## Download the data
[TPIC17 Download Link](https://drive.google.com/open?id=0B7yqoohfGsHNUmEyeVVtai12YjA)
