# Create a Database using Amazon RDS or Amazon DynamoDB
> 最後編輯時間: 2021-04-20
## 事前準備
1. Download [20210412_Cloud_Computing_Database_Services.ipynb](https://github.com/sefx5ever/SCU_Cloud_Computing_with_Fintech/blob/main/20210412_Cloud_Computing_Database_Services.ipynb)
2. Download [MySQL Workbench](https://dev.mysql.com/downloads/file/?id=500617)
3. `pip install boto3`
4. `pip install awscli`
5. `pip install mysql-connector-python`
6. Download [moviedata.zip](https://docs.aws.amazon.com/zh_tw/amazondynamodb/latest/developerguide/GettingStarted.Python.02.html)

## 大致步驟
1. 開啟ipynb程式碼檔案
2. 登入aws educate
3. 獲取token放入aws的變數中
4. 完成 案例 1：【S3】上傳 index.html
6. 完成 案例 2：【RDS】完成 CRUD 操作
7. 完成 案例 3：【DynamoDB】完成 CRUD 操作


## 案例 1：【S3】上傳 index.html
1. 透過boto3建立s3橋樑
2. 印出所有bucket
3. 上傳檔案(如:index.html)至bucket
4. 確認bucket有檔案

## 案例 2：【RDS】完成 CRUD 操作
1. 前往RDS頁面，建立資料庫
2. 選擇MySQL引擎
3. 設定Database帳號與密碼
4. 選擇public
5. Creating Database
6. 回到ipynb
7. 透過mysql.connector.connect()連接上RDS
8. 透過workbench連接RDS
9. 使用ipynb進行CRUD操作，同時前往workbench確認

## 案例 3：【DynamoDB】完成 CRUD 操作
1. 前往DynamoDB頁面
2. 回到ipynb搭建dynamoDB橋梁
3. 使用橋梁進行CRUD操作
4. 解壓縮moviedata.zip
5. 將moviedata.json上傳至DynamoDB
6. 前往DynamoDB頁面確認

## 執行助教的.ipynb可能會遇到的錯誤

+ [Unable to connect MySQL Workbench to RDS instance](https://stackoverflow.com/questions/16488135/unable-to-connect-mysql-workbench-to-rds-instance)  

+ [Boto3 Client NoRegionError: You Must Specify A Region Error Only Sometimes](https://izziswift.com/boto3-client-noregionerror-you-must-specify-a-region-error-only-sometimes/)
