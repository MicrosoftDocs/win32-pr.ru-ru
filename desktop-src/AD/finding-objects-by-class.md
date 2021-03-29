---
title: Поиск объектов по классу
description: Типичные поисковые запросы для конкретного класса объектов.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Поиск объектов по классу AD
- Active Directory, использование, поиск по классу
- объект Active Directory, поиск по классу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654187"
---
# <a name="finding-objects-by-class"></a>Поиск объектов по классу

Типичные поисковые запросы для конкретного класса объектов. В следующем примере кода выполняется поиск компьютеров с расположением в сборке 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Рассмотрим, почему не используется **objectClass** . Не используйте **objectClass** без другого сравнения, содержащего индексированный атрибут. Атрибуты индекса могут повысить эффективность запроса. Атрибут **objectClass** имеет несколько значений и не индексируется. Чтобы указать тип или класс объекта, используйте **objectCategory**.

Менее эффективно:


```C++
(objectClass=computer)
```



Более эффективно:


```C++
(objectCategory=computer)
```



Имейте в виду, что в некоторых случаях необходимо использовать сочетание **objectClass** и **objectCategory** . Класс пользователя и класс Contact должны быть указаны следующим образом.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Имейте в виду, что можно искать как пользователей, так и контакты в следующих случаях.


```C++
(objectCategory=person)
```



 

 




