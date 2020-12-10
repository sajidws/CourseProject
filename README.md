# EducationalWeb

The following instructions have been tested with:
	Python 2.7 on Linux and MacOS
	Python 3.7.6 on Windows 10 Professional (Version 2004; OS Build 19041.630)

1. Install ElasticSearch from archive and start from command line
	Linux and MacOS: https://www.elastic.co/guide/en/elasticsearch/reference/current/targz.html
	Windows 10: https://www.elastic.co/guide/en/elasticsearch/reference/current/zip-windows.html

2. Install all pre-requisite packages for this project
	`pip install -r requirements.txt` from `CourseProject/`
	Tested on Windows 10 with: elasticsearch 7.10.0, Flask 1.1.2, Flask-SocketIO 4.3.1, metapy 0.2.13, numpy 1.19.2, pytoml 0.1.21
	
3. Create the index in ElasticSearch
	`python create_es_index.py` from `CourseProject/`
	Note: this is required only one-time for the initial deployment`

4. Download tf_idf_outputs.zip from https://drive.google.com/file/d/19ia7CqaHnW3KKxASbnfs2clqRIgdTFiw/view?usp=sharing
	Unzip the file and place the folder 'tf_idf_outputs' under `CourseProject/static`

5. Download cs410.zip from https://drive.google.com/file/d/1Xiw9oSavOOeJsy_SIiIxPf4aqsuyuuh6/view?usp=sharing
	Unzip the file and place the folder 'cs410' under `CourseProject/pdf.js/static/slides/`
   
6. Install NPM (Node.js) for installing gulp
	Windows 10: follow step #1 in https://zestcode.co.uk/how-to-install-gulp-on-windows-10/
		Ensure PATH contains these directories in the order: C:\Users\<username>\AppData\Roaming\npm\node_modules;C:\Users\<username>\AppData\Roaming\npm;C:\Program Files\nodejs
	Note: this is required only one-time for the initial deployment

7. Install gulp
	`npm install gulp -g` from `CourseProject/pdf.js/build/generic/web`
	Note: this is required only one-time for the initial deployment

8. Start gulp server
	`gulp server` from `CourseProject/pdf.js/build/generic/web`
		Ensure PATH contains these directories in the order: C:\Users\<username>\AppData\Roaming\npm\node_modules;C:\Users\<username>\AppData\Roaming\npm;C:\Program Files\nodejs
	
8. In another terminal window, run `python app.py` from `CourseProject/`

9. Access the site that should now be available at http://localhost:8096/

