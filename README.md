# lambda-pdf-thumbnailer

Lambda function for creating pdf thumbnails.

Adapted from this [gist](https://gist.github.com/kageurufu/68667fcb6d3a08078616) and this [tutorial](http://marceloalves.com/tutorials/lambda/2016/02/26/pdf_to_image_thumbnail_using_lambda/)

See tutorial.txt, raw text paste incase the link ever dies. 

## Alterations for use in 2020:

1. ghostscript is not working in lambda anymore had to install this package: "https://github.com/sina-masnadi/node-gs/tarball/master"
npm install "https://github.com/sina-masnadi/node-gs/tarball/master"

2. Need to add 3 lambda layers for imagemagick and graphicmagick and ghostscript. Add them via these ARN's in lambda :
  arn:aws:lambda:eu-west-1:114655708991:layer:image-magick:1
  arn:aws:lambda:eu-west-1:764866452798:layer:ghostscript:8
  arn:aws:lambda:eu-west-1:175033217214:layer:graphicsmagick:2
