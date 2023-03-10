# Bitly-Data-Gathering-and-Transformation

### Problem Descripition 

In 2012, URL shortening service Bitly partnered with the US government website USA.gov to provide a feed of anonymous data gathered from users who shorten links ending with .gov or .mil.

### Objective:
- Scripting using Semi-Structured Data
- Data Transformation
- Python RegEx

The text file comes in JSON format and here are the important keys and their description. 


|key| description |
|---|-----------|
| a|Denotes information about the web browser and operating system|
| tz | time zone |
| r | URL the user come from |
| u | URL where the user headed to |
| t | Timestamp when the user start using the website in UNIX format |
| hc | Timestamp when user exit the website in UNIX format |
| cy | City from which the request intiated |
| ll | Longitude and Latitude |


## Steps:

### 1- Write a script can transform the JSON files to a DataFrame 

### 2- Create CSV file having the following columns:
- web_browser

        The web browser that has requested the service
        
- operating_sys

        operating system that intiated this request
        
- from_url

        The main URL the user came from

    **In a short format**:
    Ex: `www.facebook.com` Not:  `http://www.facebook.com/l/7AffQEFzjSi/1.usa.gov/wfLQtf`
     
    
- to_url

       The same applied like `to_url`
   
- city

        The city from which the the request was sent
    
- longitude

        The longitude where the request was sent
        
- latitude

        The latitude where the request was sent

- time_zone
        
        The time zone that the city follow
        
- time_in

        Time when the request started
        
- time_out
        
        Time when the request is ended
        
        


#### Note: We will make sure that the final dataframes have no NaNs at all.
