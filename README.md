# twitterwebsearch
The goal of this Python package is to automate the process for finding tweets 
older than several weeks.
These older tweets cannot be found using the Twitter
search API, but can be found through the web interface.


## Installation:
    pip install https://github.com/ShinNoNoir/twitterwebsearch/archive/master.zip

## Small example:

    import json
    import twitterwebsearch
    
    QUERY = '@shinnonoir since:2010-01-20 until:2010-02-01'
    
    def main():
        tweets = twitterwebsearch.search(QUERY)
        tweets = list(tweets) # convert generator into list
        print json.dumps(tweets, indent=2)
    
    if __name__ == '__main__':
        main()





