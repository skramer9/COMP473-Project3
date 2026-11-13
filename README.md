# COMP473-Project3
 this project will use a cloud-based system and a command-line based application where you send a string of words that will be parsed by backend processing and pull information from the cloud according to what you mentioned

CLI:
-q "Query the database based on other arguments"
-k "Keywords to save, or to query by if used with -q"
-s "Date saved, automatically set to date when saving by default, or used to query by date saved with -q"
-t "Time-frame to save, or to query by if used with -q. Format: M/D/Y_H-M/d/y_H"
        - Required 
          M : month (1 or 2 digit)
          D : day (1 or 2 digit)
        - Optional 
          Y : year (4 digit), if missing, assumed the current year
          H : hour 0-23, or 1-12am/pm
          - : time range, ie, 11/12-11/15. Missing start date returns all items before end date, ie -11/13. Missing end date returns all items since start date, ie 12/1-.

Each memory in the database is saved with
         - Required
           data : description of the item
           date-saved : the date the item was saved
         - Optional
           time-start : beginning time of the event
           time-end : end time of the event
          
      
