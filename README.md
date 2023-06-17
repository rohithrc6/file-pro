1. get_info(…): For every file inside folder1 (including files in sub-folders), calculates the extension
of the file (.txt, .csv, .pdf etc), the size (in bytes), a hash value based on a checksum hash technique
(MD5,SHA-256, your choice), the filename, the filepath and the date the file was modified on. Stores
this data in a file "file_info", the type of which is csv.

2. __init__(…): The constructor takes the path where folder1 is located. Then, if “file_info” file
is not present in cwd or if “file_info”’s DOM is older than 2 days, get_info(…) is run which will fetch the
most updated version of “file_info”.

3. generate_report(…) : When this is run, it generates a report on the screen with an option to save it to
file (txt or csv). It would contain the following information:
a. different types of files present in the folders (including all sub-folders)
b. mean and median size of the files (in general and by type)
c. the folder name (not including subfolders) with the largest amount of files by (i) number and
(ii) size

All the data required for this method will come from the “file_info” file. When this functionality
is executed, we check if the “file_info”’s date last modified is greater than 2 days, if it is older than 2 days
we call get_info() and overwrite the old “file_info” (and then generate the report). 
