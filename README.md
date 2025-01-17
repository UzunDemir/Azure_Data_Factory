#  Введение в Azure Data Factory

Многие организации работают с огромными объемами данных. Эти большие данные часто могут быть сырыми, неорганизованными и храниться в различных местах, таких как реляционные, нереляционные и другие системы хранения. Значительной проблемой для этих организаций является упорядочивание этих больших данных и их уточнение в действенные бизнес-идеи.

Microsoft Azure Data Factory — это управляемая облачная служба, которую можно использовать для создания действенных бизнес-инсайтов из неорганизованных данных. Она может помочь вам управлять сложными гибридными проектами по извлечению, преобразованию и загрузке (ETL), извлечению-загрузке-преобразованию и интеграции данных.

![image](https://github.com/UzunDemir/Azure_Data_Factory/assets/94790150/eb49b759-dc1a-4a7c-a518-bca5f3c1a670)

## Пример сценария
Давайте представим, что вы работаете в игровой компании, где вы собираете журналы данных, которые генерируются во время игровых сессий. Если бы вы могли проанализировать эти данные журнала, вы бы смогли получить представление о предпочтениях клиентов, демографии и поведении использования. Люди в вашей команде продаж выразили интерес к возможностям дополнительных и перекрестных продаж и задаются вопросом, могут ли эти журналы данных содержать полезную информацию. Команды разработки и технические специалисты заинтересованы в том, чтобы узнать о потенциальных проблемах с игровым опытом и о том, как новые функции могут помочь решить эти проблемы.

Ваша проблема в том, что для успешного анализа данных в журналах вам также необходимо ссылаться на данные, которые хранятся в локальных расположениях. Эти данные включают информацию о клиентах, информацию об играх и информацию о маркетинговых кампаниях. Ваша компания сохранила данные вашего игрового журнала в облачном хранилище данных и хочет, чтобы вы также использовали все локальные данные.

Для продвижения вперед в анализе данных решающим шагом является объединение локальных данных с дополнительными данными из игровых журналов. План состоит в том, чтобы обрабатывать объединенные данные с помощью Azure Analysis Services. Затем преобразованные данные будут опубликованы в облачном хранилище данных и визуализированы с помощью Power BI и других инструментов. Azure Data Factory может помочь вам достичь этой цели.

## Что мы будем делать?
В этом модуле вы узнаете, как Azure Data Factory может помочь вам организовать большие данные. Вы оцените, может ли Azure Data Factory помочь вам интегрировать ваши источники данных. Вы также опишете, как Azure Data Factory может принимать данные из локальных, многооблачных и программно-сервисных источников данных (SaaS).

## Какова главная цель?
К концу этого модуля вы узнаете больше о том, как определить, может ли Azure Data Factory помочь вам создать и запланировать рабочие процессы, управляемые данными, для приема данных из разных хранилищ данных. Вы оцените, может ли Azure Data Factory помочь вам построить сложные процессы ETL для визуального преобразования этих данных с помощью вычислительных служб или потоков данных.

Давайте начнем с обзора Azure Data Factory. Это должно помочь вам определить, является ли это хорошим выбором для организации ваших данных с целью создания бизнес-аналитики.

Azure Data Factory — это облачная служба ETL и интеграции данных, которая помогает создавать рабочие процессы на основе данных для:

* Организуйте перемещение данных.
* Масштабное преобразование данных.

Используя Azure Data Factory, вы можете реорганизовать необработанные данные в осмысленные хранилища данных и озера данных. Это позволяет вам принимать более обоснованные бизнес-решения.

## Что такое аналитика данных?
Аналитика данных — это процесс сбора необработанных данных и их изучения для вывода выводов. Это может быть сложно, если данные находятся в нескольких местах, например, в размещенных базах данных и в локальных местах.

*Необработанные данные — это данные, которые были собраны из источника и не были обработаны. Иногда их называют неорганизованными данными*

## Azure предоставляет несколько технологий, которые вы можете внедрить для помощи в аналитике данных вашей организации. Они включают:

* Аналитика Azure Synapse
* Хранилище больших двоичных объектов Azure
* Хранилище озера данных Azure
* Аналитика озера данных Azure
* Службы анализа Azure
* Azure HDInsight
* Azure Databricks
* Машинное обучение Azure

Вы можете использовать некоторые или все эти службы по мере необходимости для анализа данных вашей организации. Однако ни одна из этих служб не решает проблему интеграции данных. Интеграция данных позволяет собирать данные из нескольких источников, а затем загружать эти объединенные данные в место, подходящее для анализа данных. При необходимости вы можете преобразовать данные в ходе этого процесса. Хотя вы можете выполнять эти задачи вручную, вы можете рассмотреть возможность использования Azure Data Factory.

## Определение фабрики данных Azure
Azure Data Factory — это облачная служба интеграции данных, разработанная для удовлетворения потребностей двух конкретных сообществ, как описано в следующей таблице:

![image](https://github.com/UzunDemir/Azure_Data_Factory/assets/94790150/f098f31f-a8db-4522-ac6d-3bd0ef819e68)



Главное, что Azure Data Factory — это единый облачный сервис для интеграции данных. Он предоставляет единый набор инструментов и общий интерфейс управления для всей интеграции данных и поддерживает все ваши источники данных, где бы они ни находились.

## Как Azure Data Factory может помочь с аналитикой данных
Используя Azure Data Factory, вы можете:

Постройте сложные процессы ETL. Эти процессы могут визуально преобразовывать данные, используя потоки данных или вычислительные сервисы, такие как:

* Azure HDInsight Hadoop
* Azure Databricks
* База данных Azure SQL
Публикуйте эти преобразованные данные в хранилищах данных для использования приложениями бизнес-аналитики.

На следующем рисунке внешние источники данных подключены к Azure Data Factory. Для приема данных используется BLOB-объект хранилища, а Azure Synapse Analytics используется в качестве хранилища. Эти элементы обеспечивают оркестровку. Компоненты анализа и визуализации, Azure Analysis Service и Power BI также подключены к Azure Data Factory.

![image](https://github.com/UzunDemir/Azure_Data_Factory/assets/94790150/347a2fed-79b5-4b09-8e4d-71f6a03ef064)

## Как работает Azure Data Factory



![image](https://github.com/UzunDemir/Azure_Data_Factory/assets/94790150/4dbee6c8-769a-4fbe-a5f6-610a3890814b)


Создание [пайплайна](https://microsoftlearning.github.io/dp-203-azure-data-engineer/Instructions/Labs/10-Synpase-pipeline.html)

пароль: A12345678z!


