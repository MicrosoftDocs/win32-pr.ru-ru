---
title: Сведения об объекте Query
description: Сведения об объекте Query
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Проигрыватель Windows Media, объект Query
- Объектная модель проигрывателя Windows Media, объект Query
- Объектная модель, объект Query
- Элемент управления ActiveX проигрывателя Windows Media, объект Query
- Элемент управления ActiveX, объект Query
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Query
- Проигрыватель Windows Media Mobile, объект Query
- Объект запроса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776328"
---
# <a name="about-the-query-object"></a>Сведения об объекте Query

Объект **Query** представляет составной запрос. Создайте новый пустой объект **запроса** , вызвав *медиаколлектион*. **createQuery**. После создания объекта **запроса** можно вызвать **аддкондитион** , чтобы добавить условие в составной запрос. Каждый последующий вызов **аддкондитион** добавляет новое условие к существующему запросу с помощью логики и.

Например, предположим, что требуется создать запрос, представляющий все цифровые мультимедийные файлы, где **WM/жанр** равен «джаз», а **Автор** содержит «Джим». Можно создать составной запрос для представления этих условий с помощью следующего кода JScript:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Чтобы добавить условие в составной запрос с помощью или логики, необходимо вызвать метод **Query. бегиннекстграуп**. Этот метод сигнализирует, что предыдущая группа условий завершена и что следующий вызов **аддкондитион** представляет начало новой группы условий.

Например, чтобы создать запрос, представляющий все цифровые мультимедийные файлы, в которых **WM/жанр** равен «джаз», а **Author** содержит «Джим» или « **Author** » содержит «Дейв», можно использовать следующий пример кода:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



Чтобы выполнить составной запрос, вызовите метод **медиаколлектион. жетплайлистбикуери**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Медиаколлектион. Жетплайлистбикуери**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Объект запроса**](query-object.md)
</dt> </dl>

 

 




