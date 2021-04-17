---
title: Пограничный эффект
description: Используйте границу границы для расширения изображения с границ.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- граница границы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104547242"
---
# <a name="border-effect"></a><span data-ttu-id="ce106-104">Пограничный эффект</span><span class="sxs-lookup"><span data-stu-id="ce106-104">Border effect</span></span>

<span data-ttu-id="ce106-105">Используйте границу границы для расширения изображения с границ.</span><span class="sxs-lookup"><span data-stu-id="ce106-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="ce106-106">Этот результат можно использовать для повторения пикселов на краях изображения, переноса пикселов с противоположного конца изображения или зеркального отражения пикселов по границе точечного рисунка для расширения области растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="ce106-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="ce106-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1Border.</span><span class="sxs-lookup"><span data-stu-id="ce106-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="ce106-108">Примеры изображений</span><span class="sxs-lookup"><span data-stu-id="ce106-108">Example images</span></span>

<span data-ttu-id="ce106-109">В примерах здесь показаны выходные данные границы с использованием каждого режима.</span><span class="sxs-lookup"><span data-stu-id="ce106-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="ce106-110">Размер выходных данных неограничен, но эти изображения обрезаются вдвое в два раза.</span><span class="sxs-lookup"><span data-stu-id="ce106-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="ce106-111">Зеркальное отображение</span><span class="sxs-lookup"><span data-stu-id="ce106-111">Mirror</span></span>



| <span data-ttu-id="ce106-112">До</span><span class="sxs-lookup"><span data-stu-id="ce106-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![Снимок экрана, на котором изображено изображение перед результатом этого действия.](images/border-before.jpg) |
| <span data-ttu-id="ce106-114">После</span><span class="sxs-lookup"><span data-stu-id="ce106-114">After</span></span>                                                     |
| ![Снимок экрана, на котором показано изображение после преобразования.](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="ce106-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="ce106-116">Clamp</span></span>



| <span data-ttu-id="ce106-117">До</span><span class="sxs-lookup"><span data-stu-id="ce106-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![Снимок экрана, показывающий изображение до того, как оно будет применено к срезу.](images/border-before.jpg)     |
| <span data-ttu-id="ce106-119">После</span><span class="sxs-lookup"><span data-stu-id="ce106-119">After</span></span>                                                         |
| ![Снимок экрана, показывающий изображение после преобразования для среза.](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="ce106-121">оборачивание;</span><span class="sxs-lookup"><span data-stu-id="ce106-121">Wrap</span></span>



| <span data-ttu-id="ce106-122">До</span><span class="sxs-lookup"><span data-stu-id="ce106-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![Снимок экрана, на котором изображено изображение до того, как оно будет применено к оболочке.](images/border-before.jpg)    |
| <span data-ttu-id="ce106-124">После</span><span class="sxs-lookup"><span data-stu-id="ce106-124">After</span></span>                                                        |
| ![Снимок экрана, показывающий изображение после преобразования для переноса.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="ce106-126">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="ce106-126">Effect properties</span></span>



| <span data-ttu-id="ce106-127">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="ce106-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="ce106-128">Описание</span><span class="sxs-lookup"><span data-stu-id="ce106-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce106-129">Режим ребра X</span><span class="sxs-lookup"><span data-stu-id="ce106-129">Edge Mode X</span></span><br/> <span data-ttu-id="ce106-130">D2D1 \_ границы \_ , \_ \_ режим ребра \_ X</span><span class="sxs-lookup"><span data-stu-id="ce106-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="ce106-131">Режим ребра в направлении оси X для этого действия.</span><span class="sxs-lookup"><span data-stu-id="ce106-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="ce106-132">Для этого параметра можно задать значение "Обтекание", "перенос" или "зеркальный".</span><span class="sxs-lookup"><span data-stu-id="ce106-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="ce106-133">Дополнительные сведения см. в разделе [режимы краев](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="ce106-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="ce106-134">Тип — D2D1 \_ граница границы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ce106-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="ce106-135">Значение по умолчанию — \_ D2D1 \_ границы \_ режима ребра \_ .</span><span class="sxs-lookup"><span data-stu-id="ce106-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="ce106-136">Режим ребра Y</span><span class="sxs-lookup"><span data-stu-id="ce106-136">Edge Mode Y</span></span><br/> <span data-ttu-id="ce106-137">D2D1 \_ границы \_ , \_ режим ребра по \_ \_ оси Y</span><span class="sxs-lookup"><span data-stu-id="ce106-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="ce106-138">Режим ребра в направлении оси Y для этого действия.</span><span class="sxs-lookup"><span data-stu-id="ce106-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="ce106-139">Для этого параметра можно задать значение "Обтекание", "перенос" или "зеркальный".</span><span class="sxs-lookup"><span data-stu-id="ce106-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="ce106-140">Дополнительные сведения см. в разделе [режимы краев](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="ce106-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="ce106-141">Тип — D2D1 \_ граница границы \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ce106-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="ce106-142">Значение по умолчанию — \_ D2D1 \_ границы \_ режима ребра \_ .</span><span class="sxs-lookup"><span data-stu-id="ce106-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="ce106-143">Режимы краев</span><span class="sxs-lookup"><span data-stu-id="ce106-143">Edge modes</span></span>



| <span data-ttu-id="ce106-144">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="ce106-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="ce106-145">Описание</span><span class="sxs-lookup"><span data-stu-id="ce106-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce106-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="ce106-146">Clamp</span></span><br/> <span data-ttu-id="ce106-147">\_Зажим для \_ \_ режима границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="ce106-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="ce106-148">Повторяет Пиксели от краев изображения.</span><span class="sxs-lookup"><span data-stu-id="ce106-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="ce106-149">оборачивание;</span><span class="sxs-lookup"><span data-stu-id="ce106-149">Wrap</span></span><br/> <span data-ttu-id="ce106-150">\_Перенос границы D2D1 в \_ \_ режим ребра \_</span><span class="sxs-lookup"><span data-stu-id="ce106-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="ce106-151">Использует пиксели из противоположного конечного края изображения.</span><span class="sxs-lookup"><span data-stu-id="ce106-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="ce106-152">Зеркальное отображение</span><span class="sxs-lookup"><span data-stu-id="ce106-152">Mirror</span></span><br/> <span data-ttu-id="ce106-153">\_ \_ \_ Зеркальный режим границы \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="ce106-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="ce106-154">Отражает Пиксели относительно края изображения.</span><span class="sxs-lookup"><span data-stu-id="ce106-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="ce106-155">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="ce106-155">Output bitmap</span></span>

<span data-ttu-id="ce106-156">Размер выходного растрового изображения бесконечно для всех входных данных, за исключением входного изображения с размером 0.</span><span class="sxs-lookup"><span data-stu-id="ce106-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="ce106-157">Если высота или ширина входного изображения равна 0, то размер выходных данных равен 0.</span><span class="sxs-lookup"><span data-stu-id="ce106-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce106-158">Требования</span><span class="sxs-lookup"><span data-stu-id="ce106-158">Requirements</span></span>



| <span data-ttu-id="ce106-159">Требование</span><span class="sxs-lookup"><span data-stu-id="ce106-159">Requirement</span></span> | <span data-ttu-id="ce106-160">Значение</span><span class="sxs-lookup"><span data-stu-id="ce106-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce106-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce106-161">Minimum supported client</span></span> | <span data-ttu-id="ce106-162">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="ce106-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ce106-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce106-163">Minimum supported server</span></span> | <span data-ttu-id="ce106-164">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="ce106-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ce106-165">Header</span><span class="sxs-lookup"><span data-stu-id="ce106-165">Header</span></span>                   | <span data-ttu-id="ce106-166">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ce106-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ce106-167">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce106-167">Library</span></span>                  | <span data-ttu-id="ce106-168">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="ce106-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ce106-169">См. также</span><span class="sxs-lookup"><span data-stu-id="ce106-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce106-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ce106-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

