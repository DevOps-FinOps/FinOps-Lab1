# Лабораторная работа 1 (Amazon Web Services) - 3 вариант
# Участники команды
1. Париш Павел - капитан
2. Клопов Михаил
3. Буров Глеб
# Цель
Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. Сопоставление сервисов между разными провайдерами. Оценка возможностей миграции на отечественные сервисы.
# Сервисы от AWS
AmazonElastiCache - это такой управляемый сервис от AWS, который предоставляет доступ к бд Redis, Memcached, MongoDB, ускоряющие работу приложений с помощью кэширования (хранения часто используемых данных с возможностью быстрого доступа).

AmazonES (Amazon Elasticsearch Service) - это управляемая служба в AWS, даёт доступ к Elasticsearch (такой движок для поиска, анализа и визуализации больших данных)

AmazonQLDB (Amazon Quantum Ledger Database) - это управляемая служба в AWS, которая даёт доступ к распределенной бд на основе блокчейна. Технологии блокчейна позволяют фиксировать историю всех изменений бд и гарантируют неизменность этой истории.

awskms (AWS Key Management Service) - это управляемая служба в AWS, с помощью нее можно создавать ключи шифрования и управлять ими. Играет ключевую роль в обеспечении безопасности в облаке.

CloudHSM (Cloud Hardware Security Module) — это услуга от AWS, которая заключается в предоставлении физически защищенного оборудования (HSM) для хранения ключей шифрования.

AmazonRekognition - это сервис от AWS, анализирующий видео и изображения с помощью ИИ (распознавание лиц, объектов, текста и т. д.)

Amazon Textract  - это сервис от AWS, который извлекает текст и др. структурированные данные (например, таблицы) из PDF документов.

Amazon Lex - это услуга облачных вычислений от AWS, использующая технологии обработки речи (NLP). Позволяет создавать голосовые интерфейсы.

AWSCodePipeline - это сервис от AWS, который позволяет автоматизировать процесс непрерывной поставки (Continuous Delivery) приложений. Т е он автоматизирует переход кода в производство.

AmazonSES (Simple Email Service) - это служба электронной почты от AWS для отправки электронных писем из приложений.

AmazonSNS (Amazon Simple Notification Service) - это сервис уведомлений от AWS, который позволяет отправлять сообщения и уведомления между мобильными устройствами, почтами, HTTP-точками и др.
# Российские аналоги сервисов AWS
Yandex Managed Service for Redis - это управляемая служба от Yandex, который предоставляет доступ к бд Redis, используемой для кэширования, очередей и др. задач.

Yandex Managed Elasticsearch - управляемая служба от Yandex, предоставляющая доступ к Elasticsearch

Yandex Cloud KMS - управляемая служба от Yandex, предоставляющая доступ к ключам шифрования.

ViPNet HSM это услуга от ИнфоТеКС, которая заключается в предоставлении физически защищенного оборудования (HSM) для хранения ключей шифрования.

VK Vison - сервис от Mail.ru, использующий компьютерное зрение для извлечения текста и других структурированных данных из PDF документов, а так же распознования объектов и лиц на изображениях.

Yandex SpeechKit - сервис от Яндекс.Облака, использующий технологии обработки речи (NLP) для создания голосовых интерфейсов.

SendPulse - сервис  по отправке email, sms и веб-уведомлений

Mail.Ru Cloud Solutions - позволяет отправлять сообщения и уведомления между HTTP-точками.
# Сопоставление
Amazon ElastiCache - Yandex Managed Service for Redis

Amazon Elasticsearch Service - Yandex Managed Elasticsearch

Amazon Quantum Ledger Database - Нет российских аналогов

AWS Key Management Service - Yandex Cloud KMS

CloudHSM - ViPNet HSM

Amazon Rekognition, Amazon Textract -	VK Vison

Amazon Lex - Yandex SpeechKit

AWS CodePipeline - Нет российских аналогов

Amazon Simple Email Service - SendPulse

Amazon Simple Notification Service - Mail.Ru Cloud Solutions

# Таблица биллинга
| Service Usage Type                                                                                                                                                                                                                    | Product Code      | Usage Type               |  [lineItem/Operation] | lineItem/LineItemDescription | Russian Analogue                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|--------------------------|-----------------------|------------------------------|--------------------------------------------|
| Tax                                                                                                                                                                                                                                   | AmazonElastiCache |                          |                       | Tax%                         | Yandex Managed Service for Redis           |
| Cache your data. Design your own ElastiCache cluster by choosing a cache node type and the number of cache nodes.                                                                                                                     | AmazonElastiCache | %NodeUsage:cache%        |                       |                              | Yandex Managed Service for Redis           |
| Back up data by creating a snapshot. Use the backup to restore a cache or seed data to a new cache.                                                                                                                                   | AmazonElastiCache | %CreateCacheSnapshot%    |                       |                              | Yandex Managed Service for Redis           |
| Store backups, create a backup and restore data from a backup to a cache.                                                                                                                                                             | AmazonElastiCache | %ElastiCache:BackupUsage |                       |                              | Yandex Managed Service for Redis           |
| Tax                                                                                                                                                                                                                                   | AmazonES          |                          |                       | Tax%                         | Yandex Managed Service for Elasticsearch   |
| Transfer data to Amazon Simple Storage Service (S3)                                                                                                                                                                                   | AmazonES          | %DataTransfer%Bytes      |                       |                              | Yandex Managed Service for Elasticsearch   |
| Use AWS services with OpenSearch Service, such as Amazon S3 and AWS Glue Data Catalog                                                                                                                                                 | AmazonES          | %AWS%Bytes               |                       |                              | Yandex Managed Service for Elasticsearch   |
| Store data on Amazon EBS General Purpose SSD (gp2) volumes                                                                                                                                                                            | AmazonES          | %ES:GP2-Storage%         |                       |                              | Yandex Managed Service for Elasticsearch   |
| Store data on a magnetized medium                                                                                                                                                                                                     | AmazonES          | %ES:Magnetic-Storage     |                       |                              | Yandex Managed Service for Elasticsearch   |
| Use On-Demand or Reserved instances.                                                                                                                                                                                                  | AmazonES          | %ESInstance%             |                       |                              | Yandex Managed Service for Elasticsearch   |
| Use Provisioned IOPS (SSD) storage, you will be charged for the storage as well as the throughput you provision. However, you will not be charged for the I/Os you consume.                                                           | AmazonES          | %PIOPS%                  |                       |                              | Yandex Managed Service for Elasticsearch   |
| Use CloudFront which is a web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users through a worldwide network of data centers called edge locations. | AmazonES          | %CloudFront%             |                       |                              | Yandex Managed Service for Elasticsearch   |
| Store data in the Quantum Ledger Database                                                                                                                                                                                             | AmazonQLDB        | %Storage                 |                       |                              |                                            |
| Make write and read IO requests                                                                                                                                                                                                       | AmazonQLDB        | %IO-Request              |                       |                              |                                            |
| Tax                                                                                                                                                                                                                                   | awskms            |                          |                       | Tax%                         | Yandex Key Management Service              |
| Make API requests to AWS KMS                                                                                                                                                                                                          | awskms            | %KMS-Requests            |                       |                              | Yandex Key Management Service              |
| Generate and store KMS keys                                                                                                                                                                                                           | awskms            | %KMS-Keys                |                       |                              | Yandex Key Management Service              |
| Manage and access keys on FIPS-validated hardware, protected with customer-owned, single-tenant HSM instances that run in Virtual Private Cloud (VPC)                                                                                 | CloudHSM          | %CloudHSM%               |                       |                              | Cloud.ru Data Encryption Workshop (DEW)    |
| Extract information and insights from your images and videos using pre-trained and customizable computer vision (CV) capabilities                                                                                                     | AmazonRekognition |                          |                       |                              | Yandex Vision/VK Vision                    |
| Identify, understand, and extract data from forms using Machine Learning (ML)                                                                                                                                                         | AmazonTextract    | %FormsPagesProcessed     |                       |                              | Yandex Vision/VK Vision                    |
| Identify, understand, and extract data from tables using Machine Learning (ML)                                                                                                                                                        | AmazonTextract    | %TablesPagesProcessed    |                       |                              | Yandex Vision/VK Vision                    |
| Identify, understand, and extract data from text pages using Machine Learning (ML)                                                                                                                                                    | AmazonTextract    | %TextPagesProcessed      |                       |                              | Yandex Vision/VK Vision                    |
| Tax                                                                                                                                                                                                                                   | AmazonLex         |                          |                       | Tax%                         |                                            |
| Make responses for user requests, both text and voice, using Conversational AI                                                                                                                                                        | AmazonLex         | %Req%                    |                       |                              |                                            |
| Tax                                                                                                                                                                                                                                   | AWSCodePipeline   |                          |                       | Tax%                         |                                            |
| Make free CI/CD pipeline for free if it exists 30 days or less and didn’t have code changes running through it during the month                                                                                                       | AWSCodePipeline   | %trialPipeline%          |                       |                              |                                            |
| Make CI/CD pipeline which is active (a pipeline that has existed for more than 30 days and has at least one code change that runs through it during the month)                                                                        | AWSCodePipeline   | %activePipeline%         |                       |                              |                                            |
| Tax                                                                                                                                                                                                                                   | AmazonSES         |                          |                       | Tax%                         | Яндекс 360 для бизнеса                     |
| Receive emails paying for each recipients and send emails paying for messages according to receipt rules                                                                                                                              | AmazonSES         | %Recipients%             |                       |                              | Яндекс 360 для бизнеса                     |
| Make attachements for emails or receive emails with attachements                                                                                                                                                                      | AmazonSES         | %AttachmentsSize-Bytes   |                       |                              | Яндекс 360 для бизнеса                     |
| Receive emails paying only for completed chunks (256 KB of received data)                                                                                                                                                             | AmazonSES         | %ReceivedChunk%          |                       |                              | Яндекс 360 для бизнеса                     |
| Send messages paying for each message                                                                                                                                                                                                 | AmazonSES         | %Message%                |                       |                              | Яндекс 360 для бизнеса                     |
| Tax                                                                                                                                                                                                                                   | AmazonSNS         |                          |                       | Tax%                         | Cloud.ru Simple Message Notification (SMN) |
| Make free 1 million API request for free (Tier1)                                                                                                                                                                                      | AmazonSNS         | %Requests-Tier1          |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Make API request paying for each 1 million of requests (Tier2)                                                                                                                                                                        | AmazonSNS         | %Requests-Tier2          |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Send notifications to Android clients using Google Cloud Messaging (GCM)                                                                                                                                                              | AmazonSNS         | %DeliveryAttempts-GCM    |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Send A2P notifications via email using SMTP                                                                                                                                                                                           | AmazonSNS         | %DeliveryAttempts-SMTP   |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Send A2A notifications between HTTTPS endpoints                                                                                                                                                                                       | AmazonSNS         | %DeliveryAttempts-HTTP   |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Send A2A notifications using Amazon Simple Queue Service (SQS)                                                                                                                                                                        | AmazonSNS         | %DeliveryAttempts-SQS    |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Send A2P notifications via SMS, the price of which varies by destination country                                                                                                                                                      | AmazonSNS         | %SMS-Price%              |                       |                              |                                            |
| Send A2P notifications via SMS paying only for sent messages                                                                                                                                                                          | AmazonSNS         | %SMS-Sent%               |                       |                              |                                            |
| Send notifications to IOS clients using Apple Push Notification service (APNs)                                                                                                                                                        | AmazonSNS         | %DeliveryAttempts-APNS%  |                       |                              | Cloud.ru Simple Message Notification (SMN) |
| Send A2A notifications using AWS Lambda                                                                                                                                                                                               | AmazonSNS         | %DeliveryAttempts-LAMBDA |                       |                              | Cloud.ru Simple Message Notification (SMN) |
# Вывод
В ходе выполнения лабораторной работы были проанализированы AWS сервисы. Информация о функциональных возможностях сервисов была взята из официальной документации и использована для заполнения таблицы, содержащей информацию о типах и подтипах сервисов. Были подобраны российские аналоги практически для всех сервисов AWS. Миграция возможна только если не используются сервисы AmazonQLDB и AWS CodePipeline ввиду отсутствия российских аналогов.

