---
description: Инструкция SET задает значения PROPERTYNAME и РАНКМЕСОД для запроса.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Инструкция SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144071"
---
# <a name="set-statement"></a><span data-ttu-id="58188-103">Инструкция SET</span><span class="sxs-lookup"><span data-stu-id="58188-103">SET Statement</span></span>

<span data-ttu-id="58188-104">Инструкция SET задает значения PROPERTYNAME и РАНКМЕСОД для запроса.</span><span class="sxs-lookup"><span data-stu-id="58188-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="58188-105">PROPERTYNAME</span><span class="sxs-lookup"><span data-stu-id="58188-105">PROPERTYNAME</span></span>

<span data-ttu-id="58188-106">Можно связать свойство с понятным псевдонимом для запроса, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="58188-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="58188-107">ранкмесод</span><span class="sxs-lookup"><span data-stu-id="58188-107">RANKMETHOD</span></span>

<span data-ttu-id="58188-108">Можно указать метод ранжирования для запросов с термином «ABOUT», используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="58188-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="58188-109">Методы РАНКМЕСОД, которые могут быть заданы с помощью инструкции SET: ДЖАККАРДА коэффициент, коэффициент КОСТей и внутренний продукт.</span><span class="sxs-lookup"><span data-stu-id="58188-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



