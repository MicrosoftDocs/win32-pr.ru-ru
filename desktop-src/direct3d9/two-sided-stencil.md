---
description: Теневые тома используются для рисования теней с использованием буфера трафарета.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Набор элементов Two-Sided (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710678"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="9af63-103">Набор элементов Two-Sided (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9af63-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="9af63-104">Теневые тома используются для рисования теней с использованием буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="9af63-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="9af63-105">Приложение вычисляет теневые тома, переданные геометрией ограждения, вычисляя края силуэта и вытягивая их от света в набор трехмерных томов.</span><span class="sxs-lookup"><span data-stu-id="9af63-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="9af63-106">Затем эти тома дважды отрисовываются в буфер трафарета.</span><span class="sxs-lookup"><span data-stu-id="9af63-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="9af63-107">В ходе первой отрисовки рисуются многоугольники переднего обзора и увеличиваются значения буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="9af63-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="9af63-108">В ходе второй отрисовки рисуются многоугольники заднего вида, относящиеся к теневому тому, а значения буфера трафарета уменьшаются.</span><span class="sxs-lookup"><span data-stu-id="9af63-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="9af63-109">Как правило, значения увеличения и уменьшения уравновешивают друг друга. Однако сцена уже была отрисована с нормальной геометрией, из-за чего некоторые пиксели не прошли проверку Z-буфера при отрисовке теневого тома.</span><span class="sxs-lookup"><span data-stu-id="9af63-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="9af63-110">Значения, оставшиеся в буфере трафарета, соответствуют пикселям в тени.</span><span class="sxs-lookup"><span data-stu-id="9af63-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="9af63-111">Оставшееся содержимое буфера трафарета используется в качестве маски, чтобы выполнить альфа-смешение крупного, всеобъемлющего черного квартета со сценой.</span><span class="sxs-lookup"><span data-stu-id="9af63-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="9af63-112">Если буфер трафарета используется в качестве маски, в результате затеняются пиксели, которые находятся в тени.</span><span class="sxs-lookup"><span data-stu-id="9af63-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="9af63-113">Это означает, что теневая геометрия рисуется дважды для каждого источника света, оказывая давление на пропускную способность вершин графического процессора.</span><span class="sxs-lookup"><span data-stu-id="9af63-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="9af63-114">Для устранения этого эффекта разработана функция двустороннего трафарета.</span><span class="sxs-lookup"><span data-stu-id="9af63-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="9af63-115">При таком подходе существует два набора состояний трафарета (они указаны ниже): один — для треугольников переднего обзора, другой — для треугольников заднего вида.</span><span class="sxs-lookup"><span data-stu-id="9af63-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="9af63-116">В этом случае для каждого теневого тома рисуется по одному проходу на источник освещения.</span><span class="sxs-lookup"><span data-stu-id="9af63-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="9af63-117">Изменения API ограничиваются новым набором состояний рендеринга.</span><span class="sxs-lookup"><span data-stu-id="9af63-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="9af63-118">Новому состоянию отрисовки \_ D3DRS \_ \_ стенЦилмоде можно присвоить значение **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="9af63-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="9af63-119">По умолчанию имеет **значение false** , означающее текущее поведение (DirectX 8).</span><span class="sxs-lookup"><span data-stu-id="9af63-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="9af63-120">Если задано **значение true** (оно будет работать, только если \_ задан параметр D3DSTENCILCAPS твосидед), следующие состояния рендеринга будут применяться только к треугольникам переднего плана (по часовой стрелке).</span><span class="sxs-lookup"><span data-stu-id="9af63-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="9af63-121">Состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="9af63-121">Render state</span></span>        | <span data-ttu-id="9af63-122">Описание</span><span class="sxs-lookup"><span data-stu-id="9af63-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af63-123">D3DRS \_ стенЦилфаил</span><span class="sxs-lookup"><span data-stu-id="9af63-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="9af63-124">D3DSTENCILOP, если проверка трафарета завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9af63-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="9af63-125">D3DRS \_ стенЦилзфаил</span><span class="sxs-lookup"><span data-stu-id="9af63-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="9af63-126">D3DSTENCILOP, если пройден тест трафарета и z-тест завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9af63-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="9af63-127">D3DRS \_ стенЦилпасс</span><span class="sxs-lookup"><span data-stu-id="9af63-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="9af63-128">D3DSTENCILOP, если пройден и набор элементов, и z-тесты.</span><span class="sxs-lookup"><span data-stu-id="9af63-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="9af63-129">D3DRS \_ стенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="9af63-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="9af63-130">D3DCMPFUNC Fn.</span><span class="sxs-lookup"><span data-stu-id="9af63-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="9af63-131">Проверка набора элементов пройдена, если ((ref & Mask) стенЦилфн (маска шаблона &)) имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9af63-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="9af63-132">Новый набор состояний рендеринга применяется к треугольникам с обратным переходом (против часовой стрелки).</span><span class="sxs-lookup"><span data-stu-id="9af63-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="9af63-133">Состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="9af63-133">Render state</span></span>             | <span data-ttu-id="9af63-134">Описание</span><span class="sxs-lookup"><span data-stu-id="9af63-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af63-135">D3DRS \_ CCW \_ стенЦилфаил</span><span class="sxs-lookup"><span data-stu-id="9af63-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="9af63-136">D3DSTENCILOP, если проверка трафарета завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9af63-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="9af63-137">D3DRS \_ CCW \_ стенЦилзфаил</span><span class="sxs-lookup"><span data-stu-id="9af63-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="9af63-138">D3DSTENCILOP, если пройден тест трафарета и z-тест завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9af63-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="9af63-139">D3DRS \_ CCW \_ стенЦилпасс</span><span class="sxs-lookup"><span data-stu-id="9af63-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="9af63-140">D3DSTENCILOP, если пройден и набор элементов, и z-тесты.</span><span class="sxs-lookup"><span data-stu-id="9af63-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="9af63-141">D3DRS \_ CCW \_ стенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="9af63-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="9af63-142">Функция D3DCMPFUNC.</span><span class="sxs-lookup"><span data-stu-id="9af63-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="9af63-143">Проверка набора элементов пройдена, если ((ref & Mask) стенЦилфн (маска шаблона &)) имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9af63-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="9af63-144">Остальные состояния рендеринга набора элементов всегда применяются к треугольникам по часовой стрелке и против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="9af63-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="9af63-145">D3DRS \_ \_ \_ стенЦилмоде игнорируется для линий и спрайтов, что означает, что поведение не изменилось с DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="9af63-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="9af63-146">\_ \_ Состояния отрисовки набора элементов D3DRS CCW \* не учитываются.</span><span class="sxs-lookup"><span data-stu-id="9af63-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="9af63-147">Новый бит крепления указывает, поддерживает ли устройство эту функцию.</span><span class="sxs-lookup"><span data-stu-id="9af63-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="9af63-148">Драйверы, которые не поддерживают эту функцию, должны игнорировать эти новые состояния рендеринга.</span><span class="sxs-lookup"><span data-stu-id="9af63-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="9af63-149">Все остальные биты ограниченного набора элементов применяются к обоим режимам буферизации трафаретов.</span><span class="sxs-lookup"><span data-stu-id="9af63-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="9af63-150">Поскольку двусторонний \_ набор \_ элементов предполагает возможность рисования с помощью набора D3DCULLMODE \_ None, соответствующее ограничение должно быть установлено драйвером, если он поддерживает этот новый режим набора элементов.</span><span class="sxs-lookup"><span data-stu-id="9af63-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="9af63-151">Эта проблема должна быть реализована в лабораториях Microsoft Windows Hardware Quality Labs (WHQL).</span><span class="sxs-lookup"><span data-stu-id="9af63-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="9af63-152">Новые состояния рендеринга:</span><span class="sxs-lookup"><span data-stu-id="9af63-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="9af63-153">Новое ограничение:</span><span class="sxs-lookup"><span data-stu-id="9af63-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="9af63-154">См. также</span><span class="sxs-lookup"><span data-stu-id="9af63-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9af63-155">Методы буфера шаблона</span><span class="sxs-lookup"><span data-stu-id="9af63-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="9af63-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="9af63-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
