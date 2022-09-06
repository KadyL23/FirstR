# Exercise

>Your task is to recreate this file by providing the formatting. A completely unformatted version of the *text* will be made available, but you will need to add your own images. Images around 200x200 will work best (if they are too large your document will look nasty). You can search Google Images/Unsplash/etc by size, so you could use a search term such as `cat 200x200`

## Using and Managing Images

When images are used in a Markdown document they may come from one of two sources:

+ a URL
+ a local path

via URL

Linking an image via a URL is quite simple.

Here is a cat

![cat](https://www.japantimes.co.jp/wp-content/uploads/2020/06/np_file_17403-200x200.jpeg)

The markup is !\[alt_text](url)
>The BIG disadvantage of linking images via a URL is that unless you have control of the server they are served from they might be moved, deleted, renamed leading to an image not loading.

![Where did it go?](https://www.japantimes.co.jp/wp-content/uploads/2020/06/np_file_17403-200x200.xyz)

Notice that a missing image (there is one just above this line) does not appear at all.

from a local path

Linking a file from a local path is also easy, but requires more thought

![An image](https://th.bing.com/th/id/OIP.aK05MHDgS66aBRajghVFRgAAAA?w=122&h=144&c=7&r=0&o=5&pid=1.7)

The markup here was `![An image](..\Basics\img\blob_sign_year1.png)`

1. Although an absolute file path (one starting with a drive letter) *can* be used it is almost always a bad idea - if the image is renamed, moved, deleted, it breaks. If you copy the markdown folder to another machine it will not work there. Etc.
2. We almost always use relative paths. These describe where the image is *in relation to* the markdown file, using `.` to mean current folder and `..` to mean parent folder. So the path in the example is read as "find an img folder in the same folder as this markdown and look in there for blob_sign_year1.png".
3. Relative paths solve the problem so long as you want to give someone else a folder - but what if you need to give them a single file? The best option here is to convert your Markdown to PDF, this produces a single file with a copy of the image embedded inside it.

----------------------------------------------------------------------------------

 .It is considered good practice to avoid mixing Markdown and asset files together in the same folder, use sub-folders to group the assets by type.
