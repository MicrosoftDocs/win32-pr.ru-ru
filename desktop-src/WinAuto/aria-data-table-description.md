---
title: Предупреждение таблицы данных ARIA
description: Предупреждение таблицы данных ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- ариадататаблеварнингид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068496"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="37e61-104">Предупреждение таблицы данных ARIA</span><span class="sxs-lookup"><span data-stu-id="37e61-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="37e61-105">Текст</span><span class="sxs-lookup"><span data-stu-id="37e61-105">Text</span></span>

<span data-ttu-id="37e61-106">Таблица содержит данные, но не имеет ни сводки, ни допустимого атрибута **ARIA-DescribedBy** .</span><span class="sxs-lookup"><span data-stu-id="37e61-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="37e61-107">Тип</span><span class="sxs-lookup"><span data-stu-id="37e61-107">Type</span></span>

<span data-ttu-id="37e61-108">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="37e61-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="37e61-109">Описание</span><span class="sxs-lookup"><span data-stu-id="37e61-109">Description</span></span>

<span data-ttu-id="37e61-110">Это предупреждение относится к таблицам HTML с более чем одной ячейкой.</span><span class="sxs-lookup"><span data-stu-id="37e61-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="37e61-111">Он не применяется к таблицам, `role="presentation"` поскольку они считаются макетными таблицами.</span><span class="sxs-lookup"><span data-stu-id="37e61-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="37e61-112">Это предупреждение означает, что таблица идентифицирована как таблица данных, но для нее не определено доступное описание.</span><span class="sxs-lookup"><span data-stu-id="37e61-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="37e61-113">Не все таблицы данных должны иметь доступное описание.</span><span class="sxs-lookup"><span data-stu-id="37e61-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="37e61-114">Необходимо определить доступное описание, если пользователям требуются дополнительные сведения для понимания структуры и содержимого таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="37e61-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="37e61-115">Чтобы устранить это предупреждение, определите доступное для таблицы описание с помощью атрибута Summary или **ARIA-DescribedBy** .</span><span class="sxs-lookup"><span data-stu-id="37e61-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="37e61-116">Пример</span><span class="sxs-lookup"><span data-stu-id="37e61-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




