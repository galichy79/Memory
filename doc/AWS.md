


- [Установка AWS CLI на линукс video](https://www.youtube.com/watch?v=OTj63YEBoak)

CLI - comand line interface

Набираем в поисковике aws cli install

[Использование IAM создание Groups, Users Access Keys](https://www.youtube.com/watch?v=SeTTD2zP_3A)

Настройка AWS CLI
---

[Интерфейс командной строки AWS](https://aws.amazon.com/ru/cli/)

`aws --version`

security credentials -> create access key

`aws configure`



Default region name: eu-central-1

Default output format: json

`aws s3 ls` пролистать бакеты

`aws s3 mb s3:/aaa.hello.world` Создать бакет

`aws s3 sync . s3://aaa.hello.world` Синхронизировать текущую папку с s3 bucket aaa.hello.world

`aws s3 rb s3://aaa.hello.world --force` Удалить бакет и все содержимое. Работает если в бакете не установлен version control.

`aws s3 rm s3://aaa.hello.world/my-first-backup.bak` - удалить файл my-first-backup.bak из бакета.

`aws s3 sync s3://aaa.hello.world .` Синхронизировать содердимое бакета в текущую папку. Поведение команды зависит от того, что стоит на первом месте. Если на первом месте текущая папка - содержимоее ее копируется в с3 бакет. Если на первом месте бакет - его содержимое копируется в указанную в конце папку. 

[How to upload and download S3 buckets with the AWS CLI video](https://www.youtube.com/watch?v=J2aZodwPeQk)

[Delete S3 bucket with AWS CLI video](https://www.youtube.com/watch?v=7H8J_ZvDWQMg)




[S3 Bucket Часть-3 - Права и полисы доступа](https://www.youtube.com/watch?v=5DWHfcabnnY)

[S3 Bucket Часть-4 - Versioning, Cross-Region Replication](https://www.youtube.com/watch?v=k9wgLT4H2VM)

[S3 Bucket Часть-5 - Logging, Создание Static Web Site 09:07](https://www.youtube.com/watch?v=Ma2TtLjzyto)