# blog

When you want to write a post
1. hexo new "Post Title"
2. Do your writing and use the below command to see your changes on a local development server.
3. hexo server
4. Hexo generate
8. hexo deploy
The above will generate a static file to your gh-pages branch and then deploy it to franklynroth.me/blog

To update the master repo with your "newpost.md" This is to seperate the compiled version from the working version.
5. git add
6. git commit -m "Your Message"
7. git push origin master

gh-pages and master should never be merged, they are entirely seperate branches for a reason.
