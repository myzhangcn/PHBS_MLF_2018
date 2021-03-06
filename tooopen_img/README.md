# This is the spider to crawl pictures

The pictures we crawled from [**Toopen**](http://www.tooopen.com/img/87.aspx) are stored
in [`images/full`](../images/full) directory. Every picture's name is the SHA1 hash of its url.

The following steps helps you to reproduce the result.

1. Clone this repository to your local disk

    `git clone https://github.com/devon-ge/PHBS_MLF_2018.git`

2. Change to `tooopen_img` directory (root directory of this spider that contains `scrapy.cfg` and this `README.md`)

    `cd PHBS_MLF_2018/tooopen_img`
3. Run command `scrapy crawl tooopen[ -s CLOSESPIDER_ITEMCOUNT=60]`

Now, you can check the pictures in [`images/full`](../images/full) (automatically generated by
scrapy).

**Warning**: In step 3, `60` is the maximum number of item requests (you can use whatever you want).
The spider will keep running until all *nature* pictures are crawled if we
omit `CLOSESPIDER_ITEMCOUNT` option. That's time consuming!

Below are some examples

![example1](../images/full/0a3f8ee9153997c651b82989799800d50a462dbd.jpg) ![example2](../images/full/fb5f301c86b8e948cdb68a2e273fea24cdb8cdb1.jpg)

![example3](../images/full/1d7de482b2f5359371ffd10a551ad07a3d86246b.jpg) ![example4](../images/full/2d773493dc2415b631a66adc135e86c88e88fc03.jpg)