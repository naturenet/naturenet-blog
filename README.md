
# Blog

The default [wintersmith](https://github.com/jnordberg/wintersmith) template

# Install

	$ npm install

# Preview

	$ wintersmith preview
	

Open browser to `http://localhost:8080/naturenet-blog`

`naturenet-blog/` is needed in the address.

If port 8000 doesn't work, try a different port, such as 8089

	$ wintersmith preview -p 8089
	
	
# Add an article

* In `contents/articles`, create a new folder (e.g., mynewarticle)
* In this new folder, create a file called `index.md`
* In `index.md`, add the header (coped from another article)
* Now start write the body of the article.


# Commit Changes

Add to the git repo

	$ git add contents/articles/mynewarticle
	
To confirm this has been added

	$ git status 
	
To commit

	$ git commit -m 'I added a new article'
	
Now push to github server

	$ git push origin master
	

# Deploy

	$ git subtree push --prefix build origin gh-pages
