---
title: Создание и исполнение представления
description: Можно создать представление для данных, полученных из Active Directory. имейте в виду, что только определение представления хранится в SQL Server, а не в фактическом результирующем наборе. Поэтому вы можете получить другой результат при вызове представления позднее.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c4676154ea32dd06e39498e9f943b55d8dbf39694ab9c1005e942cad85f7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082728"
---
# <a name="creating-and-executing-a-view"></a>Создание и исполнение представления

Можно создать представление для данных, полученных из Active Directory. имейте в виду, что только определение представления хранится в SQL Server, а не в фактическом результирующем наборе. Поэтому вы можете получить другой результат при вызове представления позднее.

В следующем примере кода показано, как создать представление.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Используйте следующий код для вызова представления.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[создание разнородного объединения между SQL Server и Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




