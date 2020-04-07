Fastpages is an easy way to deploy your data science project as a blog post. Fastpages is easy to set up and allows for you to deploy jupiter notebooks with togleable settings. This is an easy way to get your jupyter notebooks out into the world in a presentable way, settings for the blog post can be done in the first cell of a jupyter notebook in a markdown cell.
```python
# "Title"
> "Awesome summary"
- toc: false
- branch: master
- badges: true
- comments: true
- categories: [fastpages, jupyter]
- image: images/some_folder/your_image.png
- hide: false
- search_exclude: true
- metadata_key1: metadata_value1
- metadata_key2: metadata_value2
```
The blog post then can look like a cleaner version of your notebook hosted on Github pages for other people to see and interact with!
