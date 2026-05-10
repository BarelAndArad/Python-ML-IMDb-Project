# Instructions for running "part1_final.ipynb" code

# Prerequisites
    Download from **[This link](https://datasets.imdbws.com/) the folllowing files:
        ''' name.basics.tsv.gz '''
        ''' title.basics.tsv.gz '''
        ''' title.principals.tsv.gz '''
        ''' title.ratings.tsv.gz '''
        ''' movie_df_final.csv '''

    Open Jupyter lab or Jupyter Notebook environment 
        Install the next Libraries from the following code: 
        # pip install pandas numpy requests beautifulsoup4 tqdm


# Part 1
    From the files has downloaded, copy each file path following the instructions: 
    Check for the next variable name following the next guide and copy the file path that belongs to it:
        file_path =  r'....../name.basics.tsv'          ##### ## under "name basics" title
        file_path_2 =  r'....../title.basics.tsv'       ##### ## under " title basics" title
        file_path_3 =  r'....../title.principals.tsv'   ##### ## under " title principals" title
        file_path_4 =  r'....../title.ratings.tsv'      ##### ## under " title ratings" title
    
    This part is for uploading the original datatsets and reading which information they bring 

**Only when the upper instructions made it can be able to run the cells**
 -----------------------------------------------------------------------
**NOTE! ** RUN THE CELLS ONLY until PART 6 - "WEB SCRAPING FROM WIKIPEDIA"**
 -----------------------------------------------------------------------

# Part 2
    This part is about assuming filters that required for the movies filternig and removing unnecessary data 
    It's filtering:
        data type of movies 
        data time of 60-300 minutes 
        data year is up to 2024 (include) 
        data names that start with Am-Az letters

**Run it cells as they are**

# Part 3
    This part merging the 4 datasets together into one full required dataset
    
**Note**: It merging one by one to ensure it merged well and by conditions and primary key that has given
    After every merge there is check-point to validate it

  **Run it cells as they are**


# Part 4 
    This part creates list of the 5 primary actors ID for each movie
    It based on the first 5 ID actors\actress that related to movie in the full dataset - as a decision

 **Run it cells as they are**


# Part 5
    This part works on removing duplicates of movies in the Data 
        That because part 4 created a lot of duplicate values 
    It enters the actors-list and keeps the first row only 
   
 **Run it cells as they are**
    
# Part 6
    This part is about web scraping from wikipedia for the whole movies that selected 
    It works on scraping missing values from the data to complete requested fields 
    The first code creates copy of 20 rows for the web-scrapped data for checking 
    The second code creates the full dataset 

## Desicions:
    Desicions of this part: 
    1) 
        As a decision:  Webscraping made for requested values only and not beyond 
        For example:  if movie has filmed in more than one country [valued "Countries" on wikipedia] it show empty box inside the data 
        Same as above for "Language column" 
    2)
        As a decision: numeric values of budget and box office are divided by Million  
        This decision makes the data much comfort to read than values that not divided 
        
## NOTE: It's running time could take more than 24 hours
    Option 1 **[RECOMMENDED]** :
        Copy the next file path (via user desktop) to Part 7:
        movie_df_file_path = r'..../movie_df_final.csv
    
    option 2 **[NOT RECOMMENDED]** : 
        Run Full part 6 - Web scraping from Wikipedia 
        Be Aware! - if there is "movie_df_final.csv" file in your PC the web-scraping code (Activate option 2) will overwrite it!


 -----------------------------------------------------------------------
### NOTE!  If option 2 selected - save the file movie_df_final.csv that created on jupyter environment and copy path from it selected file into "movie_df_file_path" variable at Part 7 
 -----------------------------------------------------------------------

# Part 7
    Check if the next file is from your path:
    movie_df_file_path = movie_df_final.csv ##[User Path]##
    
    This part works on the new data that created - both merging datasets from 'part 1' and web-scraping from 'part 6'
    It also cleanning the data from missing full data rows, average multiple values that related to the same movie and from un-relevant indexes that related to some values (originally from Wikipedia) 

    
**Run it cells as they are**

# Part 8
    This part is about fixing the dataset columns type 
    It converts few columns that required to be an other type: 
        Floates to Integers
        Validate Strings, Floates and Integers as required 

  **Run it cells as they are**

# Part 9
    This part summaries the missing values by each column 
    It lets the user understand the full-data values
    
    A decision that made - because there weren't full row of empty values (even from webscraping) the authors decided to not remove any row from their data 

**Run it cells as they are**

# Part 10
    This part save the clean data into CSV file 

**Run it cells as they are**







