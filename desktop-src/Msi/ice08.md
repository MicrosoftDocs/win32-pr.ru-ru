---
description: ICE08 проверяет, что таблица Component не содержит повторяющихся идентификаторов GUID. Каждый компонент должен иметь уникальный идентификатор GUID. Если таблица компонентов не существует, проверка не выполняется.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663680"
---
# <a name="ice08"></a><span data-ttu-id="5de86-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="5de86-105">ICE08</span></span>

<span data-ttu-id="5de86-106">ICE08 проверяет, что [Таблица Component](component-table.md) не содержит повторяющихся [идентификаторов GUID](guid.md).</span><span class="sxs-lookup"><span data-stu-id="5de86-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="5de86-107">Каждый компонент должен иметь уникальный идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="5de86-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="5de86-108">Если таблица компонентов не существует, проверка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5de86-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="5de86-109">Результат</span><span class="sxs-lookup"><span data-stu-id="5de86-109">Result</span></span>

<span data-ttu-id="5de86-110">ICE08 отправляет сообщение об ошибке, если две или более записи в столбце ComponentId таблицы Component содержат один и тот же идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="5de86-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="5de86-111">Пример</span><span class="sxs-lookup"><span data-stu-id="5de86-111">Example</span></span>

<span data-ttu-id="5de86-112">В следующем примере ICE08 будет публиковать сообщение о том, что компоненты красного и зеленого имеют одинаковые идентификаторы GUID.</span><span class="sxs-lookup"><span data-stu-id="5de86-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="5de86-113">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="5de86-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5de86-114">Компонент</span><span class="sxs-lookup"><span data-stu-id="5de86-114">Component</span></span> | <span data-ttu-id="5de86-115">ComponentId</span><span class="sxs-lookup"><span data-stu-id="5de86-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="5de86-116">Красный</span><span class="sxs-lookup"><span data-stu-id="5de86-116">Red</span></span>       | <span data-ttu-id="5de86-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="5de86-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="5de86-118">Синий</span><span class="sxs-lookup"><span data-stu-id="5de86-118">Blue</span></span>      | <span data-ttu-id="5de86-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="5de86-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="5de86-120">Зеленый</span><span class="sxs-lookup"><span data-stu-id="5de86-120">Green</span></span>     | <span data-ttu-id="5de86-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="5de86-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="5de86-122">Чтобы устранить эту ошибку, измените один из повторяющихся идентификаторов GUID.</span><span class="sxs-lookup"><span data-stu-id="5de86-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5de86-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5de86-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5de86-124">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="5de86-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



