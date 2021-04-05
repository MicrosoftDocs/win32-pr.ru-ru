---
description: У вас есть несколько параметров, которые можно использовать в запросе при запросе к классу событий, содержащему внедренные объекты. Результаты, возвращаемые запросом, зависят от формы используемого запроса.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Запрос внедренных объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812442"
---
# <a name="querying-embedded-objects"></a><span data-ttu-id="300fa-104">Запрос внедренных объектов</span><span class="sxs-lookup"><span data-stu-id="300fa-104">Querying Embedded Objects</span></span>

<span data-ttu-id="300fa-105">У вас есть несколько параметров, которые можно использовать в запросе при запросе к классу событий, содержащему внедренные объекты.</span><span class="sxs-lookup"><span data-stu-id="300fa-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="300fa-106">Результаты, возвращаемые запросом, зависят от формы используемого запроса.</span><span class="sxs-lookup"><span data-stu-id="300fa-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="300fa-107">Определения классов</span><span class="sxs-lookup"><span data-stu-id="300fa-107">Class Definitions</span></span>

<span data-ttu-id="300fa-108">В следующем примере показаны определения классов, которые используются для запросов WQL в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="300fa-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a><span data-ttu-id="300fa-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="300fa-109">Examples</span></span>

<span data-ttu-id="300fa-110">Следующий запрос возвращает оба внедренных класса: **E1** и **E2**, каждый из которых имеет **Prop1** и **Prop2** , заполненные данными.</span><span class="sxs-lookup"><span data-stu-id="300fa-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="300fa-111">Следующий запрос возвращает внедренный объект **E1** , но не заполняется **Prop1** и **Prop2** данными.</span><span class="sxs-lookup"><span data-stu-id="300fa-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="300fa-112">Следующий запрос возвращает встроенный класс **E1** только с **Prop1** , заполненными данными.</span><span class="sxs-lookup"><span data-stu-id="300fa-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="300fa-113">Следующий запрос возвращает оба внедренных класса: **E1** и **E2**, каждый из которых имеет **Prop1** и **Prop2** , заполненные данными.</span><span class="sxs-lookup"><span data-stu-id="300fa-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="300fa-114">Это эквивалентно первому запросу с использованием звездочки ( \* ) вместо указания каждого объекта и свойства.</span><span class="sxs-lookup"><span data-stu-id="300fa-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="300fa-115">См. также</span><span class="sxs-lookup"><span data-stu-id="300fa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="300fa-116">Запросы с помощью WQL</span><span class="sxs-lookup"><span data-stu-id="300fa-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 



