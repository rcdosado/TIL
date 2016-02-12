# scrape a slideshare presentation file 

this uses the wonderful Beautifulsoup library to navigate 
the html jungle of slideshare, and harvest slide links.
these links in turn will be given to CURL to directly download
to a folder named dumphere at the current directory.

downloads even non downloadable slides. 
not mine (refer to the link below)


```Python
#https://github.com/mitakalab/python-hacks
import os
import urllib2
from BeautifulSoup import BeautifulSoup

url = raw_input('Slideshare URL : ')
html = urllib2.urlopen(url).read()

soup = BeautifulSoup(html)
title = 'dumphere' #soup.title.string

images = soup.findAll('img', {'class':'slide_image'})

for image in images:
  image_url = image.get('data-full').split('?')[0]
  command = 'wget %s -P %s' % (image_url, title)
  os.system(command)

```