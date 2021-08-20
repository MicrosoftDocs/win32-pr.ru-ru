---
title: Диалект языка ADO LDAP
description: при использовании ActiveX объектов каталога (ADO) с диалектом LDAP спецификаторы атрибутов и диапазонов не требуются для кавычек.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- Интерфейс ADSI для диалектов ADO LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15dba9b7a701b792321ef327d7b5f9893ef3daa0a5eaad80ea151c2b2c90cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023992"
---
# <a name="ado-ldap-ranging-dialect"></a>Диалект языка ADO LDAP

при использовании ActiveX объектов каталога (ADO) с диалектом LDAP спецификаторы атрибутов и диапазонов не требуются для кавычек.

Ниже приведен пример диалекта ADO LDAP.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




