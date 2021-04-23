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
# <a name="about-the-query-object"></a><span data-ttu-id="b3f9b-111">Сведения об объекте Query</span><span class="sxs-lookup"><span data-stu-id="b3f9b-111">About the Query Object</span></span>

<span data-ttu-id="b3f9b-112">Объект **Query** представляет составной запрос.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="b3f9b-113">Создайте новый пустой объект **запроса** , вызвав *медиаколлектион*. **createQuery**.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="b3f9b-114">После создания объекта **запроса** можно вызвать **аддкондитион** , чтобы добавить условие в составной запрос.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="b3f9b-115">Каждый последующий вызов **аддкондитион** добавляет новое условие к существующему запросу с помощью логики и.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="b3f9b-116">Например, предположим, что требуется создать запрос, представляющий все цифровые мультимедийные файлы, где **WM/жанр** равен «джаз», а **Автор** содержит «Джим».</span><span class="sxs-lookup"><span data-stu-id="b3f9b-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="b3f9b-117">Можно создать составной запрос для представления этих условий с помощью следующего кода JScript:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="b3f9b-118">Чтобы добавить условие в составной запрос с помощью или логики, необходимо вызвать метод **Query. бегиннекстграуп**.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="b3f9b-119">Этот метод сигнализирует, что предыдущая группа условий завершена и что следующий вызов **аддкондитион** представляет начало новой группы условий.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="b3f9b-120">Например, чтобы создать запрос, представляющий все цифровые мультимедийные файлы, в которых **WM/жанр** равен «джаз», а **Author** содержит «Джим» или « **Author** » содержит «Дейв», можно использовать следующий пример кода:</span><span class="sxs-lookup"><span data-stu-id="b3f9b-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


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



<span data-ttu-id="b3f9b-121">Чтобы выполнить составной запрос, вызовите метод **медиаколлектион. жетплайлистбикуери**.</span><span class="sxs-lookup"><span data-stu-id="b3f9b-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3f9b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b3f9b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3f9b-123">**Медиаколлектион. Жетплайлистбикуери**</span><span class="sxs-lookup"><span data-stu-id="b3f9b-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="b3f9b-124">**Объектная модель проигрывателя для языков сценариев**</span><span class="sxs-lookup"><span data-stu-id="b3f9b-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="b3f9b-125">**Объект запроса**</span><span class="sxs-lookup"><span data-stu-id="b3f9b-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




