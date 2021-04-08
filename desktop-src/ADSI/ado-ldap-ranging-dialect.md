---
title: Диалект языка ADO LDAP
description: При использовании объектов каталогов ActiveX (ADO) с диалектом LDAP спецификаторы атрибутов и диапазонов не требуются для кавычек.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI для диалектов ADO LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78dc2c7ff2dbfc81a76ff582145b7cf12916439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887604"
---
# <a name="ado-ldap-ranging-dialect"></a>Диалект языка ADO LDAP

При использовании объектов каталогов ActiveX (ADO) с диалектом LDAP спецификаторы атрибутов и диапазонов не требуются для кавычек.

Ниже приведен пример диалекта ADO LDAP.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




