---
title: Перенос цветовых вызовов
description: В следующей таблице перечислены функции цвета и эквивалентные функции OpenGL компании ДИАФРАГМы.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Перенос GL по IRI, цвет
- Перенос из IRI GL, цвет
- перенос в OpenGL из IRI GL, цвет
- Перенос по стандарту OpenGL из IRI GL, цвет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774000"
---
# <a name="porting-color-calls"></a><span data-ttu-id="7f55d-107">Перенос цветовых вызовов</span><span class="sxs-lookup"><span data-stu-id="7f55d-107">Porting Color Calls</span></span>

<span data-ttu-id="7f55d-108">В следующей таблице перечислены функции цвета и эквивалентные функции OpenGL компании ДИАФРАГМы.</span><span class="sxs-lookup"><span data-stu-id="7f55d-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="7f55d-109">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="7f55d-109">IRIS GL function</span></span>                  | <span data-ttu-id="7f55d-110">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="7f55d-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="7f55d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7f55d-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7f55d-112">**c**</span><span class="sxs-lookup"><span data-stu-id="7f55d-112">**c**</span></span>                             | [<span data-ttu-id="7f55d-113">глколор</span><span class="sxs-lookup"><span data-stu-id="7f55d-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="7f55d-114">Задает цвет RGB.</span><span class="sxs-lookup"><span data-stu-id="7f55d-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="7f55d-115">**color**</span><span class="sxs-lookup"><span data-stu-id="7f55d-115">**color**</span></span>                         | [<span data-ttu-id="7f55d-116">глиндекс</span><span class="sxs-lookup"><span data-stu-id="7f55d-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="7f55d-117">Задает цветовой индекс.</span><span class="sxs-lookup"><span data-stu-id="7f55d-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="7f55d-118">**Перекрасить**</span><span class="sxs-lookup"><span data-stu-id="7f55d-118">**getcolor**</span></span>                      | <span data-ttu-id="7f55d-119">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ текущий \_ индекс GL)</span><span class="sxs-lookup"><span data-stu-id="7f55d-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="7f55d-120">Возвращает текущий индекс цвета.</span><span class="sxs-lookup"><span data-stu-id="7f55d-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="7f55d-121">**жетмколор**</span><span class="sxs-lookup"><span data-stu-id="7f55d-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="7f55d-122">Возвращает копию значений RGB для записи цветовой гиперкарты.</span><span class="sxs-lookup"><span data-stu-id="7f55d-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="7f55d-123">**гргбколор**</span><span class="sxs-lookup"><span data-stu-id="7f55d-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="7f55d-124">**глжет**( \_ текущий \_ Цвет GL)</span><span class="sxs-lookup"><span data-stu-id="7f55d-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="7f55d-125">Возвращает текущие значения цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="7f55d-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="7f55d-126">**мапколор**</span><span class="sxs-lookup"><span data-stu-id="7f55d-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="7f55d-127">**RGBcolor**</span><span class="sxs-lookup"><span data-stu-id="7f55d-127">**RGBcolor**</span></span>                      | <span data-ttu-id="7f55d-128">**глколор**</span><span class="sxs-lookup"><span data-stu-id="7f55d-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="7f55d-129">Задает цвет RGB.</span><span class="sxs-lookup"><span data-stu-id="7f55d-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="7f55d-130">**вритемаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-130">**writemask**</span></span>                     | [<span data-ttu-id="7f55d-131">**глиндексмаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="7f55d-132">Задает цветовую маску режима индексов цвета.</span><span class="sxs-lookup"><span data-stu-id="7f55d-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="7f55d-133">**вмпаккргбвритемаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="7f55d-134">**глколормаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="7f55d-135">Задает маску цветового режима RGB.</span><span class="sxs-lookup"><span data-stu-id="7f55d-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="7f55d-136">**жетвритемаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-136">**getwritemask**</span></span>                  | <span data-ttu-id="7f55d-137">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ \_ вритемаскный цвет GL)**глжет**( \_ индекс ГК \_ вритемаск)</span><span class="sxs-lookup"><span data-stu-id="7f55d-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="7f55d-138">Возвращает цветовую маску.</span><span class="sxs-lookup"><span data-stu-id="7f55d-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="7f55d-139">**гргбмаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-139">**gRGBmask**</span></span>                      | <span data-ttu-id="7f55d-140">**глжет**( \_ Цвет GL \_ вритемаск)</span><span class="sxs-lookup"><span data-stu-id="7f55d-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="7f55d-141">Возвращает цветовую маску.</span><span class="sxs-lookup"><span data-stu-id="7f55d-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="7f55d-142">**звритемаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-142">**zwritemask**</span></span>                    | [<span data-ttu-id="7f55d-143">**глдепсмаск**</span><span class="sxs-lookup"><span data-stu-id="7f55d-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="7f55d-144">Будьте внимательны при замене **звритемаск** на [**глдепсмаск**](gldepthmask.md); **глдепсмаск** принимает логический аргумент, тогда как **звритемаск** принимает битовое поле.</span><span class="sxs-lookup"><span data-stu-id="7f55d-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="7f55d-145">Если вы хотите использовать несколько цветных карт, необходимо использовать соответствующие функции цветовой карты Windows.</span><span class="sxs-lookup"><span data-stu-id="7f55d-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="7f55d-146">Таким образом, **multimap**, **онемап**, **жеткммоде**, **Сетмап** и **жетмап** не имеют эквивалентов OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7f55d-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 





