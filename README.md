# AWS-Python-lambda-layers
python lambda packages to use in lambda functions

# Description
Here is  python Numpy, Pandas, and Redis packages that can be uploads as a Lambda layer also the instructions to build your own package an upload  it to AWS

# Requirements!

  - Python 3.6
  - python-pip3
  
### Make Package

If you want to make pandas package to AWS Lambda:

```sh
$ cd AWS-Python-lambda-layers
$ mkdir build/python/lib/python3.6/site-packages/
$ pip3 install pandas -t build/python/lib/python3.6/site-packages/
```

check Packages

```sh
$ ls build/python/lib/python3.6/site-packages/
```
zip Packages

```sh
$ zip -r mypythonpackage.zip
```

# Upload on AWS
upload your new package to AWS s3 bucket and then go to your AWS lambda Console on Layer option.

- create Layer
- Name: mypythonlayer
- Description: my first  python lambda layer
- Code entry type: Upload a file from Amazon s3
- Amazon s3 Link URL: copy and paste Object URl of your package with the format (https://s3.amazonaws.com/YourBucket/mypythonpackage.zip)
- Compatible runtimes: python3.6

And finally click on Create

