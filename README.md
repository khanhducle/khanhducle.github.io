# Visual Search

Visual search is an old and well-studied topic in computer vision and is integrated into many widely-used search engines such as Google, Bing, and DuckDuckGo. Instead of submitting a keyword or text to the system and getting relevant documents back, user will submit an image and the system will return images that have similar visual contents. 
Traditional approach to web-scale image retrieval relies on bag-of-visual-words model that is initially introduced in [1]. In this model, local features such as SIFT or SURF are extracted from the query images. Those features are then assigned to their closest visual words in a visual vocabulary. A visual vocabulary is constructed by extracting local features from all of the images in the database, then using k-means clustering to find the centers of each cluster. The centers are the visual words of the vocabulary. The query image is accordingly represented by a global histogram of visual words, and matched with database images by tf-idf weighting using inverted files. This research activity will explore this techniques step by step so that the user has an overview about image retrieval in general.

# Overview of Image Search Engine
# Basic Image Search Pipeline
# Advanced Image Search (Pre-deep learning)
# Advanced Image Search (Post-deep learning)

You can use the [editor on GitHub](https://github.com/khanhducle/khanhducle.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/khanhducle/khanhducle.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
