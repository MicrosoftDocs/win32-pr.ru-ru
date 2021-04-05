---
title: Перечисление
description: Доступ к данным и управление ими с помощью ADSI предоставляет несколько примеров перечисления. Можно также перечислить дочерние элементы объектов контейнера. Эти дочерние объекты сами по себе являются объектами, а не просто свойствами объектов.
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, пример кода Visual Basic, использование Иадсконтаинер для перечисления объектов
- контейнеры ADSI, использование Иадсконтаинер для перечисления дочерних элементов контейнера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986108"
---
# <a name="enumeration"></a>Перечисление

[Доступ к данным и управление ими с помощью ADSI](accessing-and-manipulating-data-with-adsi.md) предоставляет несколько примеров перечисления. Можно также перечислить дочерние элементы объектов контейнера. Эти дочерние объекты сами по себе являются объектами, а не просто свойствами объектов.

В следующем примере используется интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) для перечисления дочерних элементов контейнера.


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




