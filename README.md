# catify

## A simple hysds job that generates a composite jpg image.

### Usage

1. Select the `catify-product` dataset in [HySDS Facet Search](https://ec2-54-84-150-28.compute-1.amazonaws.com/search)
2. Using `On-Demand` option, enter a Tag, and select Action "Catify [production]"
3. Scroll down to the `base_image_url` field, and enter the url of a jpg image, e.g. https://vignette.wikia.nocookie.net/the-martian/images/f/f9/JPL.jpg
4. Once the job completes, as indicated in [HySDS Resource Management](https://ec2-54-86-171-31.compute-1.amazonaws.com/figaro), you may then view the output composite image by drilling down into the [corresponding S3 folder](https://s3.console.aws.amazon.com/s3/buckets/maapdev/products/catify/?region=us-east-1).

### Developer Notes

This job uses a custom [HySDS Dataset Specification](https://github.com/hysds/hysds-framework/wiki/Datasets) to designate a 'catify' S3 folder for storing its output. The image overlay script is implemented in the [Catify.py](Catify.py) script, which downloads the input file and overlays our [fatcat.jpg](fatcat.jpg), to validate a trivial data ingestion exercise. 
