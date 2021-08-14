# Week 2 Scripting Like A Developer

The code found in this repository will help you script like a developer.

## WIP
The code found in Week 2 Scripting Like A Developer is currently a work in progress and the readme will be updated when ready.
 
## Python Code
The Python Code found in Week 2 Scripting Like A Developer is for anyone that wants to create a resource group in AWS

## How to use Python Code
The s3bucket.py script is designed to be reused at any point for any environment. There are no hard-coded values.

## Examples

```Python
import sys
import boto3

try:
    def main():
        create_s3bucket(bucket_name)

except Exception as e:
    print(e)

def create_s3bucket(bucket_name):
    s3_bucket=boto3.client(
        's3',
    )

    bucket = s3_bucket.create_bucket(
        Bucket=bucket_name,
        ACL='private',
        )

    print(bucket)

bucket_name = sys.argv[1]

if __name__ == '__main__':
    main()

python s3bucket.py 'cloudskillss3bucket'
```

## Test 
Python code have unit test available to ensure that the desired outcomes, including values and types, are accurate.

## Contributors
1. Devin Radford 