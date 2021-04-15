---
title: Диалект языка многомерных объектов ADO SQL
description: При использовании объектов каталогов ActiveX (ADO) с использованием диалекта SQL необходимо использовать одинарные кавычки (') в отношении атрибута и спецификатора диапазона.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- Многодиалектный интерфейс ADSI в ADO SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7b846cd3517613dd8ea914f53a7b31c30f8651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654161"
---
# <a name="ado-sql-ranging-dialect"></a>Диалект языка многомерных объектов ADO SQL

При использовании объектов каталогов ActiveX (ADO) с использованием диалекта SQL необходимо использовать одинарные кавычки (') в отношении атрибута и спецификатора диапазона. Ниже приведен пример диалекта ADO SQL.


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




