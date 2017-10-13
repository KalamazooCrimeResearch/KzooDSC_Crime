#INFORMATION FOR MAKE ON WINDOWS
#Make can be downloaded here: https://www.gnu.org/software/make/
#http://gnuwin32.sourceforge.net/packages/coreutils.htm
#adding this to your path will give you some necessary linux commands.

#INFORMATION FOR MAKE ON MAC OS
# https://stackoverflow.com/questions/1469994/using-make-on-osx 
BALT_URL = "https://data.baltimorecity.gov/api/views/xviu-ezkt/rows.csv?accessType=DOWNLOAD"
CINC_URL = "https://data.cincinnati-oh.gov/api/views/4try-zhpp/rows.csv?accessType=DOWNLOAD"
SEAT_URL = "https://data.seattle.gov/api/views/3k2p-39jp/rows.csv?accessType=DOWNLOAD"
#FOR TESTING MAKE:
IRIS_URL = "https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data"

#this will remove any raw data csvs.

#these are not related to file structure.
.PHONY: all clean


all: data/raw/cincinnati.csv
	data/raw/cincinnati.csv

clean:
	rm -f data/raw/*.csv
data/raw/baltimorecity.csv:
	python data/download.py $(CINC_URL) $@
data/raw/cincinnati.csv:
	python data/download.py $(BALT_URL) $@

data/raw/seattle.csv:
	python data/download.py $(SEAT_URL) $@
	
data/raw/iris.csv:
	python data/download.py $(IRIS_URL) $@

	

