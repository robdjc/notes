Example commands to tar/untar log and configuration directories: 

`tar -czvf logfolder.tar.gz logfolder`

`tar -xzvf logfolder.tar.gz`


Example commands to untar a specific file from an archive: 

`tar -xzvf logfolder.tar.gz filename.log`


Example command to view the files in a tar file:

`tar -tzvf logfolder.tar.gz`


Example command to send files from a tar to stdout:

`tar -xOf logs.tar.gz *file_pattern*`
