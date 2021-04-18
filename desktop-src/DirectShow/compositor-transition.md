---
description: Переход компоновщика
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Переход компоновщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553777"
---
# <a name="compositor-transition"></a><span data-ttu-id="0fd8a-103">Переход компоновщика</span><span class="sxs-lookup"><span data-stu-id="0fd8a-103">Compositor Transition</span></span>

> [!Note]  
> <span data-ttu-id="0fd8a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-104">\[Deprecated.</span></span> <span data-ttu-id="0fd8a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0fd8a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0fd8a-106">Переход компоновщика совмещенный прямоугольник от переднего плана к заданному прямоугольнику в фоновом режиме без изменения остальной части фона.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-106">The Compositor transition composites a subrectangle from the foreground into a designated rectangle on the background, without altering the rest of the background.</span></span> <span data-ttu-id="0fd8a-107">Используйте этот переход для создания эффектов "разделить на экран" или "изображение в виде изображения".</span><span class="sxs-lookup"><span data-stu-id="0fd8a-107">Use this transition to create split-screen or picture-in-picture effects.</span></span>

<span data-ttu-id="0fd8a-108">На следующем рисунке показан переход компоновщика:</span><span class="sxs-lookup"><span data-stu-id="0fd8a-108">The following image shows the compositor transition:</span></span>

![Переход компоновщика](images/trans-compositor.png)

<span data-ttu-id="0fd8a-110">Идентификатор класса (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span><span class="sxs-lookup"><span data-stu-id="0fd8a-110">Class ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}</span></span>

<span data-ttu-id="0fd8a-111">Имя переменной CLSID: CLSID \_ дксткомпоситор</span><span class="sxs-lookup"><span data-stu-id="0fd8a-111">CLSID Variable Name: CLSID\_DxtCompositor</span></span>

<span data-ttu-id="0fd8a-112">Понятное имя: "Дксткомпоситор"</span><span class="sxs-lookup"><span data-stu-id="0fd8a-112">Friendly Name: "DxtCompositor"</span></span>

<span data-ttu-id="0fd8a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0fd8a-113">Properties</span></span>



| <span data-ttu-id="0fd8a-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="0fd8a-114">Property</span></span>   | <span data-ttu-id="0fd8a-115">Тип</span><span class="sxs-lookup"><span data-stu-id="0fd8a-115">Type</span></span> | <span data-ttu-id="0fd8a-116">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="0fd8a-116">Default</span></span> | <span data-ttu-id="0fd8a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0fd8a-117">Description</span></span>                                                    |
|------------|------|---------|----------------------------------------------------------------|
| <span data-ttu-id="0fd8a-118">Высота</span><span class="sxs-lookup"><span data-stu-id="0fd8a-118">Height</span></span>     | <span data-ttu-id="0fd8a-119">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-119">long</span></span> | <span data-ttu-id="0fd8a-120">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-120">0</span></span>       | <span data-ttu-id="0fd8a-121">Высота целевого прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-121">Height of the target rectangle, in pixels.</span></span>                     |
| <span data-ttu-id="0fd8a-122">OffsetX</span><span class="sxs-lookup"><span data-stu-id="0fd8a-122">OffsetX</span></span>    | <span data-ttu-id="0fd8a-123">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-123">long</span></span> | <span data-ttu-id="0fd8a-124">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-124">0</span></span>       | <span data-ttu-id="0fd8a-125">Горизонтальное смещение целевого прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-125">Horizontal offset of the target rectangle, in pixels.</span></span>          |
| <span data-ttu-id="0fd8a-126">OffsetY</span><span class="sxs-lookup"><span data-stu-id="0fd8a-126">OffsetY</span></span>    | <span data-ttu-id="0fd8a-127">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-127">long</span></span> | <span data-ttu-id="0fd8a-128">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-128">0</span></span>       | <span data-ttu-id="0fd8a-129">Вертикальное смещение целевого прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-129">Vertical offset of the target rectangle, in pixels.</span></span>            |
| <span data-ttu-id="0fd8a-130">срчеигхт</span><span class="sxs-lookup"><span data-stu-id="0fd8a-130">SrcHeight</span></span>  | <span data-ttu-id="0fd8a-131">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-131">long</span></span> | <span data-ttu-id="0fd8a-132">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-132">0</span></span>       | <span data-ttu-id="0fd8a-133">Высота подпрямоугольника в источнике (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-133">The height of the subrectangle on the source, in pixels.</span></span>       |
| <span data-ttu-id="0fd8a-134">сркоффсеткс</span><span class="sxs-lookup"><span data-stu-id="0fd8a-134">SrcOffsetX</span></span> | <span data-ttu-id="0fd8a-135">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-135">long</span></span> | <span data-ttu-id="0fd8a-136">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-136">0</span></span>       | <span data-ttu-id="0fd8a-137">Координата по оси x подпрямоугольника в источнике (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-137">The x-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="0fd8a-138">сркоффсети</span><span class="sxs-lookup"><span data-stu-id="0fd8a-138">SrcOffsetY</span></span> | <span data-ttu-id="0fd8a-139">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-139">long</span></span> | <span data-ttu-id="0fd8a-140">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-140">0</span></span>       | <span data-ttu-id="0fd8a-141">Координата по оси y подпрямоугольника в источнике (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-141">The y-coordinate of the subrectangle on the source, in pixels.</span></span> |
| <span data-ttu-id="0fd8a-142">срквидс</span><span class="sxs-lookup"><span data-stu-id="0fd8a-142">SrcWidth</span></span>   | <span data-ttu-id="0fd8a-143">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-143">long</span></span> | <span data-ttu-id="0fd8a-144">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-144">0</span></span>       | <span data-ttu-id="0fd8a-145">Ширина подпрямоугольника в источнике (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-145">The width of the subrectangle on the source, in pixels.</span></span>        |
| <span data-ttu-id="0fd8a-146">Ширина</span><span class="sxs-lookup"><span data-stu-id="0fd8a-146">Width</span></span>      | <span data-ttu-id="0fd8a-147">long</span><span class="sxs-lookup"><span data-stu-id="0fd8a-147">long</span></span> | <span data-ttu-id="0fd8a-148">0</span><span class="sxs-lookup"><span data-stu-id="0fd8a-148">0</span></span>       | <span data-ttu-id="0fd8a-149">Ширина целевого прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-149">Width of the target rectangle, in pixels.</span></span>                      |



 

<span data-ttu-id="0fd8a-150">Эти свойства показаны на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="0fd8a-150">The following diagram illustrates these properties:</span></span>

![свойства компоновщика](images/compmeasure.png)

## <a name="related-topics"></a><span data-ttu-id="0fd8a-152">См. также</span><span class="sxs-lookup"><span data-stu-id="0fd8a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd8a-153">Переходы и эффекты</span><span class="sxs-lookup"><span data-stu-id="0fd8a-153">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> </dl>

 

 



