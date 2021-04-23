---
title: Создание и исполнение представления
description: Можно создать представление для данных, полученных из Active Directory. Имейте в виду, что только определение представления хранится в SQL Server, а не в фактическом результирующем наборе. Поэтому вы можете получить другой результат при вызове представления позднее.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410605"
---
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="fe719-105">Создание и исполнение представления</span><span class="sxs-lookup"><span data-stu-id="fe719-105">Creating and Executing a View</span></span>

<span data-ttu-id="fe719-106">Можно создать представление для данных, полученных из Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fe719-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="fe719-107">Имейте в виду, что только определение представления хранится в SQL Server, а не в фактическом результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="fe719-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="fe719-108">Поэтому вы можете получить другой результат при вызове представления позднее.</span><span class="sxs-lookup"><span data-stu-id="fe719-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="fe719-109">В следующем примере кода показано, как создать представление.</span><span class="sxs-lookup"><span data-stu-id="fe719-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="fe719-110">Используйте следующий код для вызова представления.</span><span class="sxs-lookup"><span data-stu-id="fe719-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="fe719-111">См. также</span><span class="sxs-lookup"><span data-stu-id="fe719-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe719-112">Создание разнородного объединения между SQL Server и Active Directory</span><span class="sxs-lookup"><span data-stu-id="fe719-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




