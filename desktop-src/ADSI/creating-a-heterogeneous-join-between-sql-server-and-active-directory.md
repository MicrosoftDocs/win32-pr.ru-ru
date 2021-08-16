---
title: создание разнородного объединения между &ами SQL Server Active Directory
description: Все сотрудники корпорации Fabrikam рассматриваются каждые шесть месяцев.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8620706db56124b83c8cd8151c067a548d5a73d557fa6523ed82167647450b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840294"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>создание разнородного объединения между &ами SQL Server Active Directory

Все сотрудники корпорации Fabrikam рассматриваются каждые шесть месяцев. Оценки проверки хранятся в базе данных отдела кадров в SQL Server. Чтобы создать представление этих данных, Джо Ворден, администратор предприятия, должен сначала создать таблицу "Оценка производительности сотрудников".

в анализаторе запросов SQL Joe джо создает таблицу с именем "проверка EMP" \_ , которая будет содержать три столбца для хранения имени сотрудника, дату проверки и рейтинг, полученный сотрудником.


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



теперь джо может присоединить Active Directory пользовательские объекты к таблице SQL Server.

В этом примере инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) содержит список данных, которые будут получены из службы каталогов и SQL Server. Инструкция [from](https://msdn.microsoft.com/library/Aa258869.aspx) содержит имя связанного сервера каталогов, с которого эти сведения будут получены из, в данном случае виевадусерс. Оператор [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) предоставляет условия поиска. в этом примере поиск выполняется по имени в службе каталогов, для которой задано SQL имя пользователя, указанное в предыдущей задаче.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



предыдущая команда возвращает результат из обеих SQL Server и Active Directory. путь AdsPath и заголовок относятся к Active Directory, в то время как имя пользователя, ReviewDate и оценка относятся к таблице SQL. Он даже может создать другое представление для этого объединения.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




