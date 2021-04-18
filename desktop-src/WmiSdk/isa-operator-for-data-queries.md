---
description: Используйте оператор ISA в предложении WHERE запроса данных, чтобы запросить внедренные объекты в иерархии классов.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Оператор ISA для запросов данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683895"
---
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="3c21f-103">Оператор ISA для запросов данных</span><span class="sxs-lookup"><span data-stu-id="3c21f-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="3c21f-104">Используйте оператор ISA в предложении WHERE запроса данных, чтобы запросить внедренные объекты в иерархии классов.</span><span class="sxs-lookup"><span data-stu-id="3c21f-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="3c21f-105">В следующем примере показан синтаксис для запроса внедренных объектов в иерархии классов.</span><span class="sxs-lookup"><span data-stu-id="3c21f-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="3c21f-106">Результат включает в себя экземпляры **класса** , содержащие внедренные объекты, которые являются производными от **паренткласс** в свойстве **ембеддедпроп** .</span><span class="sxs-lookup"><span data-stu-id="3c21f-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="3c21f-107">Не каждый экземпляр объекта **класса** является производным от **паренткласс**, но результат возвращает внедренные объекты, которые являются производными от **паренткласс**.</span><span class="sxs-lookup"><span data-stu-id="3c21f-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="3c21f-108">Например, в следующем запросе **класс** a содержит слабо типизированное свойство **ембеддедобж** .</span><span class="sxs-lookup"><span data-stu-id="3c21f-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="3c21f-109">Класс **класса** a имеет десять экземпляров.</span><span class="sxs-lookup"><span data-stu-id="3c21f-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="3c21f-110">Пять из этих экземпляров имеют внедренные объекты с типом, производным от **классз**.</span><span class="sxs-lookup"><span data-stu-id="3c21f-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="3c21f-111">Другие пять имеют внедренные объекты других типов.</span><span class="sxs-lookup"><span data-stu-id="3c21f-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="3c21f-112">В следующем примере показан запрос, возвращающий пять экземпляров, которые включают объекты, производные от **классз**.</span><span class="sxs-lookup"><span data-stu-id="3c21f-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



