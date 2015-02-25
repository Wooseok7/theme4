---
layout: post
title: “알고보면 쉬운 웹서비스”
categories: 
tag: 
date:   2014-08-29 14:10:17
---



{% highlight python %}
if __name__ =='__main__':
	img_thread = threading.Thread(target=downloadWallpaper)
	img_thread.start()
	st = '\rDownloading Image'
	current = 1
	while img_thread.is_alive():
		sys.stdout.write(st+'.'*((current)%5))
		current=current+1
		time.sleep(0.3)
	img_thread.join()
	print('\nImage of the day downloaded.')
{% endhighlight %}
















