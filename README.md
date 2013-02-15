**Demo:** [https://dl.dropbox.com/u/2848831/thoughtbox/index.html](https://dl.dropbox.com/u/2848831/thoughtbox/index.html)

## Wat? 

Thoughbox is most likely a badly written attempt at creating a markdown post system running out of a Dropbox public folder. I don't have a blog or a way to keep track of my newly found code tricks, I love markdown and want to write with it even when I have nothing to say, and finally, it's Valentine's day night, and I need a creative outlet.

I wanted an easier way to publish content without having to setup a Wordpress site or even having to log into an admin to publish stuff. I am fully aware of solutions like Jekyll and Octopress for a different approach and emphasis to publishing but they are more than I really need to quickly post something.

Thoughtbox works on top of Dropbox, jQuery, MarkdownConverter and Masonery with a little Bootstrap for added sexiness. Third-party resources are loaded via CDN (CloudFlare), and the JS to output the posts is in the index file.

## Getting setup

1. Setup a dropbox account with a *public folder*. We need this so we can copy and access the files via their public links. The "Share link" option will not work as it just redirects you to a page with a download button, but feel free to try. Dropbox has now disabled default public folders for new accounts ([from their website](https://www.dropbox.com/help/16/en): "*Please note: New Dropbox accounts created after October 4, 2012 no longer have a Public folder.*"). If necessary, re-enable it by visiting [www.dropbox.com/enable_public_folder](https://www.dropbox.com/enable_public_folder) (clicking it will not murder your dropbox).

2. Copy the files from this repo into a directory inside your public repo, call it whatever you want - we'll call it "thoughtbox" for the sake of consistency. 

3. Get the public link for any of the files you just uploaded to that folder and edit the "path" variable in the ```index.html``` file on line 

4. You should now have something like: 
		
		<script type="text/javascript">
			var path = 'https://dl.dropbox.com/u/########/thoughtbox/';
		</script>
	
5. In the "*thoughtbox*" folder look at the demo ```db.md```. This file serves as the post database. One markdown post url per line, no more, no less, and *absolutely* no space between lines. Delete the demo urls from the file and replace them with your own. Use ***https***:// otherwise you'll get see a "Can't display post" error due to the browser complaining about "insecure content".

6. Copy the public link to ```index.html```, paste in your browser's URL bar and voilà! Le tour est joué. You should see whatever posts were loaded in your ```db.md``` file.

7. For extra awesomeness, point a domain to it or something.
8. There is no 8.

## todo

1. Rewrite readme.
2. Support single posts view, with URL history.
3. Add pagination.
4. Parse published date
5. Add tag indexing/category filtering.
