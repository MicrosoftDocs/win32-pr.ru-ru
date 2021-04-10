---
description: ICE95 проверяет таблицу управления и таблицу Ббконтрол, чтобы убедиться, что элементы управления объявления помещаются на все объявления.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266128"
---
# <a name="ice95"></a><span data-ttu-id="8b3bf-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="8b3bf-103">ICE95</span></span>

<span data-ttu-id="8b3bf-104">ICE95 проверяет таблицу [управления](control-table.md) и [таблицу ббконтрол](bbcontrol-table.md) , чтобы убедиться, что элементы управления объявления помещаются на все объявления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="8b3bf-105">Результат</span><span class="sxs-lookup"><span data-stu-id="8b3bf-105">Result</span></span>

<span data-ttu-id="8b3bf-106">Если одно из следующих условий истинно, элемент управления "объявление" не поместится на объявление.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="8b3bf-107">ICE95 отправляет следующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="8b3bf-108">Предупреждение ICE95</span><span class="sxs-lookup"><span data-stu-id="8b3bf-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="8b3bf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8b3bf-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3bf-110">Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="8b3bf-111">Координата X превышает границу минимальной ширины элемента управления на стенде% s</span><span class="sxs-lookup"><span data-stu-id="8b3bf-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="8b3bf-112">Координата X элемента управления находится за пределами ширины объявления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="8b3bf-113">Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="8b3bf-114">Координата Y превышает границу минимальной высоты элемента управления на стенде% s</span><span class="sxs-lookup"><span data-stu-id="8b3bf-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="8b3bf-115">Координата Y элемента управления находится ниже нижней границы объявления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="8b3bf-116">Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="8b3bf-117">Координата X и ширина вместе превышают минимальную ширину элемента управления "объявление"% s</span><span class="sxs-lookup"><span data-stu-id="8b3bf-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="8b3bf-118">Координата X элемента управления и ширина элемента управления выходят за пределы ширины объявления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="8b3bf-119">Элемент Ббконтрол " \[ 1 \] . \[ 2 \] "в таблице ббконтрол не умещается во всех элементах управления" объявление "в таблице управления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="8b3bf-120">Координата Y и высота вместе превышают минимальную высоту элемента управления на стенде% s</span><span class="sxs-lookup"><span data-stu-id="8b3bf-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="8b3bf-121">Координата Y элемента управления плюс высота элемента управления ниже нижней границы объявления.</span><span class="sxs-lookup"><span data-stu-id="8b3bf-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="8b3bf-122">Пример</span><span class="sxs-lookup"><span data-stu-id="8b3bf-122">Example</span></span>

<span data-ttu-id="8b3bf-123">ICE95 сообщает о следующих предупреждениях для примера:</span><span class="sxs-lookup"><span data-stu-id="8b3bf-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="8b3bf-124">Таблица управления (частичная) (частичная)</span><span class="sxs-lookup"><span data-stu-id="8b3bf-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="8b3bf-125">Control</span><span class="sxs-lookup"><span data-stu-id="8b3bf-125">Control</span></span>  | <span data-ttu-id="8b3bf-126">Тип</span><span class="sxs-lookup"><span data-stu-id="8b3bf-126">Type</span></span>      | <span data-ttu-id="8b3bf-127">Ширина</span><span class="sxs-lookup"><span data-stu-id="8b3bf-127">Width</span></span> | <span data-ttu-id="8b3bf-128">Высота:</span><span class="sxs-lookup"><span data-stu-id="8b3bf-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="8b3bf-129">control1</span><span class="sxs-lookup"><span data-stu-id="8b3bf-129">control1</span></span> | <span data-ttu-id="8b3bf-130">Печат</span><span class="sxs-lookup"><span data-stu-id="8b3bf-130">Billboard</span></span> | <span data-ttu-id="8b3bf-131">300</span><span class="sxs-lookup"><span data-stu-id="8b3bf-131">300</span></span>   | <span data-ttu-id="8b3bf-132">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-132">100</span></span>    |
| <span data-ttu-id="8b3bf-133">Control2</span><span class="sxs-lookup"><span data-stu-id="8b3bf-133">Control2</span></span> | <span data-ttu-id="8b3bf-134">Печат</span><span class="sxs-lookup"><span data-stu-id="8b3bf-134">Billboard</span></span> | <span data-ttu-id="8b3bf-135">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-135">100</span></span>   | <span data-ttu-id="8b3bf-136">300</span><span class="sxs-lookup"><span data-stu-id="8b3bf-136">300</span></span>    |



 

[<span data-ttu-id="8b3bf-137">Таблица Ббконтрол</span><span class="sxs-lookup"><span data-stu-id="8b3bf-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="8b3bf-138">Печат\_</span><span class="sxs-lookup"><span data-stu-id="8b3bf-138">Billboard\_</span></span> | <span data-ttu-id="8b3bf-139">ббконтрол</span><span class="sxs-lookup"><span data-stu-id="8b3bf-139">BBControl</span></span>  | <span data-ttu-id="8b3bf-140">X</span><span class="sxs-lookup"><span data-stu-id="8b3bf-140">X</span></span>   | <span data-ttu-id="8b3bf-141">Да</span><span class="sxs-lookup"><span data-stu-id="8b3bf-141">Y</span></span>   | <span data-ttu-id="8b3bf-142">Ширина</span><span class="sxs-lookup"><span data-stu-id="8b3bf-142">Width</span></span> | <span data-ttu-id="8b3bf-143">Высота:</span><span class="sxs-lookup"><span data-stu-id="8b3bf-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="8b3bf-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="8b3bf-144">billboard1</span></span>  | <span data-ttu-id="8b3bf-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="8b3bf-145">bbcontrol1</span></span> | <span data-ttu-id="8b3bf-146">200</span><span class="sxs-lookup"><span data-stu-id="8b3bf-146">200</span></span> | <span data-ttu-id="8b3bf-147">0</span><span class="sxs-lookup"><span data-stu-id="8b3bf-147">0</span></span>   | <span data-ttu-id="8b3bf-148">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-148">100</span></span>   | <span data-ttu-id="8b3bf-149">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-149">100</span></span>    |
| <span data-ttu-id="8b3bf-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="8b3bf-150">billboard1</span></span>  | <span data-ttu-id="8b3bf-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="8b3bf-151">bbcontrol2</span></span> | <span data-ttu-id="8b3bf-152">0</span><span class="sxs-lookup"><span data-stu-id="8b3bf-152">0</span></span>   | <span data-ttu-id="8b3bf-153">200</span><span class="sxs-lookup"><span data-stu-id="8b3bf-153">200</span></span> | <span data-ttu-id="8b3bf-154">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-154">100</span></span>   | <span data-ttu-id="8b3bf-155">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-155">100</span></span>    |
| <span data-ttu-id="8b3bf-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="8b3bf-156">billboard1</span></span>  | <span data-ttu-id="8b3bf-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="8b3bf-157">bbcontrol3</span></span> | <span data-ttu-id="8b3bf-158">50</span><span class="sxs-lookup"><span data-stu-id="8b3bf-158">50</span></span>  | <span data-ttu-id="8b3bf-159">0</span><span class="sxs-lookup"><span data-stu-id="8b3bf-159">0</span></span>   | <span data-ttu-id="8b3bf-160">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-160">100</span></span>   | <span data-ttu-id="8b3bf-161">50</span><span class="sxs-lookup"><span data-stu-id="8b3bf-161">50</span></span>     |
| <span data-ttu-id="8b3bf-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="8b3bf-162">billboard1</span></span>  | <span data-ttu-id="8b3bf-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="8b3bf-163">bbcontrol4</span></span> | <span data-ttu-id="8b3bf-164">0</span><span class="sxs-lookup"><span data-stu-id="8b3bf-164">0</span></span>   | <span data-ttu-id="8b3bf-165">50</span><span class="sxs-lookup"><span data-stu-id="8b3bf-165">50</span></span>  | <span data-ttu-id="8b3bf-166">50</span><span class="sxs-lookup"><span data-stu-id="8b3bf-166">50</span></span>    | <span data-ttu-id="8b3bf-167">100</span><span class="sxs-lookup"><span data-stu-id="8b3bf-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="8b3bf-168">См. также</span><span class="sxs-lookup"><span data-stu-id="8b3bf-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b3bf-169">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="8b3bf-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



