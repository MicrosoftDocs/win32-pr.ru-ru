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
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="5272e-103">Создание разнородного объединения между &ами SQL Server Active Directory</span><span class="sxs-lookup"><span data-stu-id="5272e-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="5272e-104">Все сотрудники корпорации Fabrikam рассматриваются каждые шесть месяцев.</span><span class="sxs-lookup"><span data-stu-id="5272e-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="5272e-105">Оценки проверки хранятся в базе данных отдела кадров в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5272e-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="5272e-106">Чтобы создать представление этих данных, Джо Ворден, администратор предприятия, должен сначала создать таблицу "Оценка производительности сотрудников".</span><span class="sxs-lookup"><span data-stu-id="5272e-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="5272e-107">В анализаторе запросов SQL Сергей собирается создать таблицу с именем "Проверка EMP" \_ , которая будет содержать три столбца для хранения имени сотрудника, дату проверки и рейтинг, полученный сотрудником.</span><span class="sxs-lookup"><span data-stu-id="5272e-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="5272e-108">Сергей может вставить несколько записей.</span><span class="sxs-lookup"><span data-stu-id="5272e-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="5272e-109">Теперь Джо может присоединить Active Directory пользовательские объекты к таблице SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5272e-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="5272e-110">В этом примере инструкция [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) содержит список данных, которые будут получены из службы каталогов и SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5272e-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="5272e-111">Инструкция [from](https://msdn.microsoft.com/library/Aa258869.aspx) содержит имя связанного сервера каталогов, с которого эти сведения будут получены из, в данном случае виевадусерс.</span><span class="sxs-lookup"><span data-stu-id="5272e-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="5272e-112">Оператор [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) предоставляет условия поиска.</span><span class="sxs-lookup"><span data-stu-id="5272e-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="5272e-113">В этом примере выполняется поиск по имени в службе каталогов, для которого задано имя пользователя SQL, указанное в предыдущей задаче.</span><span class="sxs-lookup"><span data-stu-id="5272e-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="5272e-114">Предыдущая команда возвращает результат из обеих SQL Server и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5272e-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="5272e-115">Путь AdsPath и заголовок относятся к Active Directory, в то время как имя пользователя, ReviewDate и оценка относятся к таблице SQL.</span><span class="sxs-lookup"><span data-stu-id="5272e-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="5272e-116">Он даже может создать другое представление для этого объединения.</span><span class="sxs-lookup"><span data-stu-id="5272e-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




