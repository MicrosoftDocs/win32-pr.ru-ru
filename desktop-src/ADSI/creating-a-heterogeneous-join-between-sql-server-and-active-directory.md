---
title: Создание разнородного объединения между &ами SQL Server Active Directory
description: Все сотрудники корпорации Fabrikam рассматриваются каждые шесть месяцев.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103987217"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Создание разнородного объединения между &ами SQL Server Active Directory

Все сотрудники корпорации Fabrikam рассматриваются каждые шесть месяцев. Оценки проверки хранятся в базе данных отдела кадров в SQL Server. Чтобы создать представление этих данных, Джо Ворден, администратор предприятия, должен сначала создать таблицу "Оценка производительности сотрудников".

В анализаторе запросов SQL Сергей собирается создать таблицу с именем "Проверка EMP" \_ , которая будет содержать три столбца для хранения имени сотрудника, дату проверки и рейтинг, полученный сотрудником.


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



Сергей может вставить несколько записей.


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



Теперь Джо может присоединить Active Directory пользовательские объекты к таблице SQL Server.

В этом примере инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) содержит список данных, которые будут получены из службы каталогов и SQL Server. Инструкция [from](https://msdn.microsoft.com/library/Aa258869.aspx) содержит имя связанного сервера каталогов, с которого эти сведения будут получены из, в данном случае виевадусерс. Оператор [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) предоставляет условия поиска. В этом примере выполняется поиск по имени в службе каталогов, для которого задано имя пользователя SQL, указанное в предыдущей задаче.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



Предыдущая команда возвращает результат из обеих SQL Server и Active Directory. Путь AdsPath и заголовок относятся к Active Directory, в то время как имя пользователя, ReviewDate и оценка относятся к таблице SQL. Он даже может создать другое представление для этого объединения.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




