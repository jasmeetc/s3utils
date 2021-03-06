s3utils
=======
[![Build Status](https://secure.travis-ci.org/jasmeetc/s3utils.png)](http://travis-ci.org/jasmeetc/s3utils)
[![Code Climate](https://codeclimate.com/badge.png)](https://codeclimate.com/github/jasmeetc/s3utils)
[![Dependency
Status](https://gemnasium.com/jasmeetc/s3utils.png)](https://gemnasium.com/jasmeetc/s3utils)

Ruby s3 utils that use AWS SDK to work easily with IAM roles.

Installation
-------------

    gem install s3utils

Setting up gem
---------------

AWS configuration is taken from one of the following places in the order
given:

 1. If Environment Variable AWS_CREDENTIAL_FILE is set, it will
    look in the file. The file should have at least two lines:·


AWSAccessKeyId=A34554D...

AWSSecretKey=ACF4545666...
 2. Environment Variables:
    AWS_ACCESS_KEY_ID and
    AWS_SECRET_ACCESS_KEY 
    
 3. If you are running this in an EC2 instance with IAM role, this will
    automatically pick up the configuration

Proxy Settings
------------

If you are behind a proxy, set the environment variable:
HTTPS_PROXY='https://user:password@my.proxy:443/'

Commands available after install
----------------------------

      s3cmd createbucket name                 # creates a bucket
      s3cmd deletebucket name [--force]       # deletes a bucket, if it is empty. --force will delete a non-empty bucket
      s3cmd deletekey bucket:key [--prefix]   # deletes a key in the given bucket. --prefix will delete all keys in the bucket with the prefix
      s3cmd get bucket:key file               # get the file for the key from the bucket
      s3cmd get_timestamp bucket:key          # get the last modified integer timestamp for the key from the bucket
      s3cmd help [TASK]                       # Describe available tasks or one specific task
      s3cmd list bucket:prefix                # list the keys of a bucket
      s3cmd listbuckets                       # lists all of the buckets in your account
      s3cmd move bucket:key bucket:key        # moves a file from one bucket to another
      s3cmd copy bucket:key bucket:key        # copies a file from one bucket to another
      s3cmd put bucket:key file               # puts a file for the key in the bucket
      s3cmd version                           #  gives the version of s3utils gem



Please Feel free to leave any issue you find
