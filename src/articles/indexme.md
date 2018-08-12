`indexme`
=========

`indexme`, when run inside a directory, creates an index.html and a .indexme 
file in there. The .indexme file has some preferences as explained below, and 
the index.html file contains the directory listing.

<pre>
USAGE: indexme [-q] [-arczh] [dir ...]
  -q  Operate quietly (overrides -v).
  -v  Verbose mode (overrides -q).
  -r  Index recursively (obeys ignore/include directives).
  -a  Index all directories containing a .indexme file and exit.
  -c  Display a line for crontab and exit.
  -z  Launch a daemon that runs -a every 60 seconds.
  -h  Display this help message and exit.

ENVIRONMENT
  I_TITLE     Page title.
              Currently: 'articles'
  I_CSS_URL   URL of stylesheet
              Currently: 'index.css'
  I_JS_URL    URL of script.
              Currently: 'index.js'
  I_CSS_FILE  Set to directly embed stylesheet
              Currently: ''
  I_JS_FILE   Set to directly embed script
              Currently: ''
  I_LSFLAGS   Flags sent to ls(1) Ex: -c to sort by date.
              Currently: '-A'
  I_INCLUDE   Regex to whitelist entries
              Currently: '.*'
  I_IGNORE    Regex to blacklist entries, overrides I_INCLUDE
              Currently: '^index.html\|.indexme$'
  I_OUT       Output file
              Currently: 'index.html'
  I_QUIET     Set to suppress messages
              Currently: ''
  I_RECURSIVE Set to index subdirectories (obeys include/ignore).
              Currently: ''

  These variables are assigned in the following places:
    1. Defaults initialized
    2. Command-line arguments
    3. source ~/.indexme_profile
    4. source .indexme
</pre>
