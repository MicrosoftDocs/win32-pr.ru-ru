---
title: Воздействие на насыщенность
description: Используйте этот результат, чтобы изменить насыщенность изображения.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- воздействие на насыщенность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071498"
---
# <a name="saturation-effect"></a><span data-ttu-id="a8067-104">Воздействие на насыщенность</span><span class="sxs-lookup"><span data-stu-id="a8067-104">Saturation effect</span></span>

<span data-ttu-id="a8067-105">Используйте этот результат, чтобы изменить насыщенность изображения.</span><span class="sxs-lookup"><span data-stu-id="a8067-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="a8067-106">Воздействие на насыщенность — это специализация [цветовой матрицы](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="a8067-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="a8067-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1Saturation.</span><span class="sxs-lookup"><span data-stu-id="a8067-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="a8067-108">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="a8067-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="a8067-109">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="a8067-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a8067-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a8067-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a8067-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a8067-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="a8067-112">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="a8067-112">Example image</span></span>

<span data-ttu-id="a8067-113">В этом примере показаны входные и выходные изображения для эффектов насыщенности с насыщенностью 0%.</span><span class="sxs-lookup"><span data-stu-id="a8067-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="a8067-114">До</span><span class="sxs-lookup"><span data-stu-id="a8067-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)  |
| <span data-ttu-id="a8067-116">После</span><span class="sxs-lookup"><span data-stu-id="a8067-116">After</span></span>                                                       |
| ![изображение после преобразования.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="a8067-118">Этот результат вычисляет цветовую матрицу на основе значения насыщенности *в* уравнении здесь, которое указывается с помощью \_ \_ \_ Свойства насыщенности D2D1 насыщенности.</span><span class="sxs-lookup"><span data-stu-id="a8067-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="a8067-119">Уравнение матрицы показано здесь.</span><span class="sxs-lookup"><span data-stu-id="a8067-119">The matrix equation is shown here.</span></span>

![Формула для вычисления матрицы насыщенности.](images/saturation-formula.png)

<span data-ttu-id="a8067-121">Созданная матрица зависит только от значения насыщенности.</span><span class="sxs-lookup"><span data-stu-id="a8067-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="a8067-122">Если требуется определенная матрица, можно использовать [цветовую матрицу](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="a8067-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="a8067-123">Этот результат использует и выводит предварительно умноженные альфа-изображения.</span><span class="sxs-lookup"><span data-stu-id="a8067-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="a8067-124">Этот результат не будет работать с прямыми альфа-изображениями, если они не полностью непрозрачны.</span><span class="sxs-lookup"><span data-stu-id="a8067-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="a8067-125">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="a8067-125">Effect properties</span></span>



| <span data-ttu-id="a8067-126">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="a8067-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="a8067-127">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8067-127">Type and default value</span></span>           | <span data-ttu-id="a8067-128">Описание</span><span class="sxs-lookup"><span data-stu-id="a8067-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8067-129">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="a8067-129">Saturation</span></span><br/> <span data-ttu-id="a8067-130">\_Насыщенность D2D1 насыщенности перегрузки \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8067-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="a8067-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a8067-131">FLOAT</span></span><br/> <span data-ttu-id="a8067-132">0,5 f</span><span class="sxs-lookup"><span data-stu-id="a8067-132">0.5f</span></span><br/> | <span data-ttu-id="a8067-133">Насыщенность изображения.</span><span class="sxs-lookup"><span data-stu-id="a8067-133">The saturation of the image.</span></span> <span data-ttu-id="a8067-134">Можно задать для насыщенности значение от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="a8067-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="a8067-135">Если задать для него значение 1, выходное изображение будет полностью насыщенным.</span><span class="sxs-lookup"><span data-stu-id="a8067-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="a8067-136">Если задать для него значение 0, выходное изображение будет монохромным.</span><span class="sxs-lookup"><span data-stu-id="a8067-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="a8067-137">Значение насыщенности является бесмодульным.</span><span class="sxs-lookup"><span data-stu-id="a8067-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a8067-138">Требования</span><span class="sxs-lookup"><span data-stu-id="a8067-138">Requirements</span></span>



| <span data-ttu-id="a8067-139">Требование</span><span class="sxs-lookup"><span data-stu-id="a8067-139">Requirement</span></span> | <span data-ttu-id="a8067-140">Значение</span><span class="sxs-lookup"><span data-stu-id="a8067-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8067-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8067-141">Minimum supported client</span></span> | <span data-ttu-id="a8067-142">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="a8067-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a8067-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8067-143">Minimum supported server</span></span> | <span data-ttu-id="a8067-144">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="a8067-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a8067-145">Header</span><span class="sxs-lookup"><span data-stu-id="a8067-145">Header</span></span>                   | <span data-ttu-id="a8067-146">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="a8067-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="a8067-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8067-147">Library</span></span>                  | <span data-ttu-id="a8067-148">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="a8067-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="a8067-149">См. также</span><span class="sxs-lookup"><span data-stu-id="a8067-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8067-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="a8067-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

