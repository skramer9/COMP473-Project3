# COMP473-Project3
 this project will use a cloud-based system and a command-line based application where you send a string of words that will be parsed by backend processing and pull information from the cloud according to what you mentioned

## CLI:
    -q ... "Query the database based on other arguments"
    -k keywords "Keywords to save, or to query by if used with -q. Comma separated list of key words for query, unformulated string for saving."
             With -q:
                -k "Search for memories with ONE OR MORE of these keywords"
                -K "Search for memories with ALL of these keywords"
    -s date "Date saved, automatically set to date when saving by default, or used to query by date saved with -q. Format same as below."
    -t time-frame "Time-frame to save, or to query by if used with -q. Format: M/D/Y_H-M/d/y_H"
            - Required 
              M : month (1 or 2 digit)
              D : day (1 or 2 digit)
            - Optional 
              Y : year (4 digit), if missing, assumed the current year
              H : hour 0-23, or 1-12am/pm
              - : time range, ie, 11/12-11/15. Missing start date returns all items before end date, ie -11/13. Missing end date returns all items since start date, ie 12/1-.
     -d id "delete memory with the given id"
     -e id ... "edit the memory with the given id using additional arguments, ie -e memory1 -t '11/1-' would change the time-frame of memory1 to 11/1-"

## Each memory in the database is saved with (in addition to their generated id)
         - Required
           data : description of the item
           date-saved : the date the item was saved
           user : the user that the memory belongs to (only this user can access the memory)
         - Optional
           time-start : beginning time of the event
           time-end : end time of the event

## Users in the database are saved with
    - UserID
    - Password
    - Date created
