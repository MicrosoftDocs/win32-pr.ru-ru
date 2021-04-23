---
description: Предложение WHERE в запросе указывает набор элементов для сопоставления с результатами.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Функция Реусевхере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701383"
---
# <a name="reusewhere-function"></a><span data-ttu-id="e6563-103">Функция Реусевхере</span><span class="sxs-lookup"><span data-stu-id="e6563-103">ReuseWhere Function</span></span>

<span data-ttu-id="e6563-104">Предложение [WHERE](-search-sql-where.md) в запросе указывает набор элементов для сопоставления с результатами.</span><span class="sxs-lookup"><span data-stu-id="e6563-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="e6563-105">Последующие запросы могут совместно использовать работу, выполненную для предыдущего запроса, с помощью функции Реусевхере в новом предложении WHERE запроса.</span><span class="sxs-lookup"><span data-stu-id="e6563-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="e6563-106">Запросы, использующие эту функцию, выполняются быстрее.</span><span class="sxs-lookup"><span data-stu-id="e6563-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="e6563-107">Примеры</span><span class="sxs-lookup"><span data-stu-id="e6563-107">Examples</span></span>

<span data-ttu-id="e6563-108">В следующем сценарии показано, как использовать функцию Реусевхере:</span><span class="sxs-lookup"><span data-stu-id="e6563-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="e6563-109">Вы выполните следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="e6563-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="e6563-110">В возвращенном наборе строк вы получаете [идентификатор WHERE](-search-sql-rowset-properties.md), *Query1WhereID*.</span><span class="sxs-lookup"><span data-stu-id="e6563-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="e6563-111">Идентификатор WHERE является свойством набора строк с параметром PROPs {aa6ee6b0-e828-11D0-B2-3E-00-AA-00-47-FC-01}, PROPID 8 и типом UI4.</span><span class="sxs-lookup"><span data-stu-id="e6563-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="e6563-112">Вы выдаете второй запрос с помощью функции Реусевхере, передавая *Query1WhereID* из шага 2:</span><span class="sxs-lookup"><span data-stu-id="e6563-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="e6563-113">Второй запрос эквивалентен следующему:</span><span class="sxs-lookup"><span data-stu-id="e6563-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="e6563-114">Функцию Реусевхере можно использовать анвхере в предложении [WHERE](-search-sql-where.md) .</span><span class="sxs-lookup"><span data-stu-id="e6563-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6563-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e6563-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e6563-116">**Reference**</span><span class="sxs-lookup"><span data-stu-id="e6563-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6563-117">Предложения WHERE</span><span class="sxs-lookup"><span data-stu-id="e6563-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="e6563-118">Свойства набора строк</span><span class="sxs-lookup"><span data-stu-id="e6563-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



