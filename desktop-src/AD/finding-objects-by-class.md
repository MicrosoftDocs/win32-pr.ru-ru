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
ms.openlocfilehash: e81d90dbcd50a3ce001c1dec57d8fafb0f1987376cf71314902b7f035f923512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189173"
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



 

 




