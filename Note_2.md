# Polarishub_flask

## Logic

### /polarishub_flask

- \__init__.py
  - Define a name for the project(?)
- activate.sh  
  - Activate the virtual environment
- app.py
  - open the browser http://localhost:5000/, and run the app at 0.0.0.0:5000
- requirement.txt
  - pip freeze --local > requirements.txt
- run_flask.sh
  - run app.py

### /Files/about.html

​	The ***about*** page  

### /server

Encounter new packages in python: os, sys

```python
import os
from datetime import datetime

print(os.getcwd())

os.chdir('/Users/kicka/Documents/GitHub')

print(os.getcwd())
print(os.listdir())

'''
os.mkdir('test1') # only 1 level deep directory
os.makedirs('test1/test2') # can go deeper
os.rmdir('test1') # doesn't work, has subdirectory
os.removedirs('test1/test2')
'''

print(os.listdir()) 

mod_time = os.stat('zychenn_notes').st_mtime # time stamp of last modification time
print(datetime.fromtimestamp(mod_time))

#for dirpaths, dirnames, filenames in os.walk(os.getcwd()):
#    print(dirpaths,dirnames,filenames)

os.environ.get('WINDIR')

os.path.join(a,b)
os.path.basename()
os.path.dirname()
os.path.split()
os.path.exists()
os.path.isdir()
os.path.isfile()
os.path.splitext()

path1 = os.path.dirname(__file__)
print(path1) # the direct directory


path2 = os.path.dirname(os.path.dirname(__file__)) #
print(path2) # the upper directory

path6 = os.__file__ 
print(path6) # where os.py is
```

```python
import sys

sys.stderr.write('This is stderr text\n')
sys.stderr.flush()
sys.stdout.write('This is stdout\n')

print(sys.argv) # pass argument from cmd

if len(sys.argv) >1:
    print(sys.argv[1])
```



- \__init__.py
  
```python

sys.path.insert(0, os.path.dirname(os.path.abspath(__file__)))  # change the priority sys path to the current directory
os.chdir(os.path.dirname(os.path.dirname(os.path.abspath(__file__)))) # change the directory to the polaris_flask directory
```

- @app.route('/')
  - redirect the route to the /files/
- @app.route('/files/', defaults = {"filename":""})
- @app.route('/files/\<path:filename>', methods=['GET', 'POST'])
  - The most essential part, that is get files and post files in this web page.
  - it includes variable URL and default value is ""
- @app.route('/opendir')
  - Open directory in user's computer
- @app.route('/settings')
  - the setting page, which allows users to set their username.
- @app.route('/temp/\<path:temppath>')
  - send the files to others, using `send_file`, in Flask.
- @app.route('/qr', methods = ['POST'])
  - generate QR code
- @app.route("/about")
  - Return about.html page
- @app.route('/update_settings', methods = ["POST"])
  - Use to update username
- @app.route('/halt')
  - Turn off Polarishub
- @app.route('/help')
  - Return help.html
