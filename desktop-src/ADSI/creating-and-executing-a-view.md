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
# <a name="creating-and-executing-a-view"></a>Создание и исполнение представления

Можно создать представление для данных, полученных из Active Directory. Имейте в виду, что только определение представления хранится в SQL Server, а не в фактическом результирующем наборе. Поэтому вы можете получить другой результат при вызове представления позднее.

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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание разнородного объединения между SQL Server и Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




