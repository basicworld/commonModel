## rabbit

an easy to use tool kit for python, function include: email, time, csv, xls, zip...

### defore use

1. python version 2.7x required

2. you should install packages in file `dependence`

	pip install -r dependence

Note that some packages is not easy to install, eg lxml, pillow.
you should google for method

### imgetter

function: a function to download img using url

	imgetter(url)

### filesplitter(*args, **kwargs)

function: split file(s) into small size

	splited_file_names = filesplitter(filename1, filename2, size=10)

### func_monitor

function: a decorator to show runnig time of func


	@func_monitor()
	def func():
		pass

### time_builder

function: a function to build time

	time_builder()
	>>> '2016-02-15'

	time_builder('20160215')
	>>> '2016-02-15'

	time_builder('2016-02-15', 1)
	>>> '2016-02-16'

	time_builder('2016-02-15', -1)
	>>> '2016-02-14'

### lister

function: convert *args to one list

	lister(1,2,(3,4))
	>>>[1,2,3,4]

	lister(1,2,(3,4.1), target_type=int)
	>>>[1,2,3,4]

	lister(1,2,(3,4),[[5,6],7])
	>>>[1,2,3,4,5,6,7]


### distinct

function; delete all duplicate items in *args and return list

	distinct(1,2,2,3,(4,4,5,6))
	>>>[1,2,3,4,5,6]

### filer

function: create filedir and return abspath of file

	filer('name.txt', './')
	>>> '/root/rabbit/name.txt'

### logger

function: use logging easily

	lg = logger('file', 'logname.log', '/your/log/dir')
	lg.error('error')
	lg.info('running well')

### tree

functions: a good function to create default dict

	a = tree()
	a['a']['b']['c'] = 1
	print a['a']['b']['c']

### csv2xls

function: change csv file to xls

warning: lines of csv file must<=65535

### CsvManager

class: create csv file

	csvapp = CsvManager('csvname.csv')
	csvapp.writerow(1,2,3,(4,5))

### MySQLManager

class: connect to mysql

api is same as MySQLdb

### XlsManager

class: create xls file

### ZipManager

class: create zip file from files or from dir

### EmailSender

class: send email

	eapp = EmailSender()
	eapp.to = 'test@example.com'
	eapp.sugject = 'hello'
	eapp.body = 'world'
	eapp.send()

### EmailGetter

class: get email

in developing...
