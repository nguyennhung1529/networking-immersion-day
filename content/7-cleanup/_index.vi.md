+++
title = "Dọn dẹp tài nguyên"
date = 2021
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### 1. Clear S3 bucket
  - Truy cập [S3 console](https://s3.console.aws.amazon.com/s3/home).
  - Tích chọn S3 bucket của bạn, và click vào **Empty**.
    ![S3](/images/7.clean/001-S3-empty-s3-bucket.png)
  - Nhập **permanently delete**.
  - Click **Empty**.
    ![S3](/images/7.clean/002-S3-empty-s3-bucket.png)

#### 2. Xóa S3 bucket
  - Truy cập [S3 console](https://s3.console.aws.amazon.com/s3/home).
  - Tích chọn S3 bucket của bạn, và click vào **Delete**.
    ![S3](/images/7.clean/003-S3-delete-s3-bucket.png)
  - Nhập tên bucket của bạn.
  - Click **Delete bucket**.
    ![S3](/images/7.clean/004-S3-delete-s3-bucket.png)

#### 3. Xóa CloudFront Distribution
  - Truy cập [Cloufront console](https://us-east-1.console.aws.amazon.com/cloudfront/v4/home).
  - Tích chọn Cloufront distribution cần disable, và click vào **Diable**.
    ![CF](/images/7.clean/005-CF-disable-CF-distribution.png)
  - Click **Disable**.
    ![CF](/images/7.clean/005-CF-disable-CF-distribution.png)
  - Chờ cho tới khi Cloudfront distribution diasble (bạn có thể xem ở phần **Last modified**, nếu hiển thị ngày giờ thì tức đã disable thành công).
  - Quay trở lại [Cloufront console](https://us-east-1.console.aws.amazon.com/cloudfront/v4/home). Tích chọn Cloufront distribution cần delete, và click vào **Delete**.
    ![CF](/images/7.clean/007-CF-delete-CF-distribution.png)
  - Click **Delete**.
    ![CF](/images/7.clean/008-CF-delete-CF-distribution.png)

#### 5. Xóa DNS record sets
  - Truy cập [Route 53](https://us-east-1.console.aws.amazon.com/route53/v2/home).
  - Chọn **Hosted zones** ở trên thanh điều hướng phía bên trái.
  - Click chọn hosted zones của bạn.
  - Chọn các records mà bạn đã tạo, và click **Delete records**.
    ![Route53](/images/7.clean/009-Route53-delete-record.png)
  - Click **Delete**.
    ![Route53](/images/7.clean/010-Route53-delete-record.png)

#### 6. Xóa User và Policies
##### Xóa User bạn đã tạo ở bước trước đấy
  - Truy cập IAM console.
  - Truy cập **Users**.
  - Chọn user `GitHub-Actions`.
  - Click **Delete**.
    ![IAM](/images/7.clean/011-IAM-delete-user.png)
  - Nhập tên user.
  - Click **Delete**.
    ![IAM](/images/7.clean/012-IAM-delete-user.png)

##### Xóa Policy bạn đã tạo ở bước trước đấy
  - Truy cập IAM console.
  - Truy cập **Policies**.
  - Chọn policy `DeployWebsite`.
  - Click **Delete**.
    ![IAM](/images/7.clean/013-IAM-delete-policy.png)
  - Nhập tên policy.
  - Click **Delete**.
    ![IAM](/images/7.clean/014-IAM-delete-policy.png)