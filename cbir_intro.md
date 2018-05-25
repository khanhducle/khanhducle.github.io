# Overview of Image Search Engine

We're all familiar with text based search engines such as Google, Bing, and DuckDuckGo - you simply enter a few keywords related to the content you want to find (i.e., your "query"), and then your results are returned to you. But for the image search engines, things work a little differently - you're not using _text_ as your query, you are instead using an _image_

In general, there tend to be 3 types of image search engines: **search by meta-data**, **search by example**, and a **hybrid approach** of the two

## Search by Meta-Data
Search by meta-data is only marginally different the the standard keyword-based search engines mentioned above. Search by meta-data systems rarely examine the contents of the image itself. Instead, they rely on textual clues such as (1) manual annotions and tagging performed by humans along with (2) automated contextual hints, such as the text that appears near the image on a webpage.

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/cbir_flickr_example.jpg" alt>
    <b>Example of a Search by meta-data</b>
</p>

When a user performs a search on a search by meta-data system they provide a query, just like in a traditional text search engine, and then images that have similar tags or annotations are returned. The actual image itself is rarely examined.

A great example of a Search by Meta-Data system is Flickr. After uploading an image to Flickr you are presented with a text field to enter tags describing the contents of images you have uploaded. Flickr then takes these keywords, indexes them, and utilizes them to find and recommend other relevant images.

## Search by Example
Search by example systems, on the other hand, rely solely on the contents of the image — no keywords are assumed to be provided. The image is analyzed, quantified, and stored so that similar images are returned by the system during a search.

<p align="center">
    <img src="https://github.com/khanhducle/khanhducle.github.io/blob/master/images/tineye_market.PNG" alt>
    <b>Example of a Search by Example on TinEye</b>
</p>

Image search engines that quantify the contents of an image are called Content-Based Image Retrieval (CBIR) systems. The term CBIR is commonly used in the academic literature, but in reality, it’s simply a fancier way of saying “image search engine” with the added poignancy that the search engine is relying strictly on the contents of the image and not any textual annotations associated with the image.

A great example of a Search by Example system is TinEye. TinEye is actually a reverse image search engine where you first provide a query image, and then TinEye returns near-identical matches of the same image, along with the webpage that the original image appeared on.
