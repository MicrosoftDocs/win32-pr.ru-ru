---
title: Морфологи, результат
description: Используйте морфологиный результат к границам тонкого или сиккенного периметра изображения.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- эффекты морфологи
- непоздний результат
- разрушить, результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136598"
---
# <a name="morphology-effect"></a><span data-ttu-id="d3cfe-106">Морфологи, результат</span><span class="sxs-lookup"><span data-stu-id="d3cfe-106">Morphology effect</span></span>

<span data-ttu-id="d3cfe-107">Используйте морфологиный результат к границам тонкого или сиккенного периметра изображения.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="d3cfe-108">Этот результат создает ядро, в котором в два раза больше заданные значения ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="d3cfe-109">Этот результат выравнивает ядро на раздельном пикселе и возвращает максимальное значение в ядре (если дилатинг) или минимальное значение в ядре (если еродинг).</span><span class="sxs-lookup"><span data-stu-id="d3cfe-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="d3cfe-110">Идентификатором CLSID для этого действия является CLSID \_ D2D1Morphology.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="d3cfe-111">Примеры изображений</span><span class="sxs-lookup"><span data-stu-id="d3cfe-111">Example images</span></span>

<span data-ttu-id="d3cfe-112">В этом примере показаны выходные данные этого действия при использовании режима разрушить.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="d3cfe-113">До</span><span class="sxs-lookup"><span data-stu-id="d3cfe-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| <span data-ttu-id="d3cfe-115">После</span><span class="sxs-lookup"><span data-stu-id="d3cfe-115">After</span></span>                                                      |
| ![изображение после преобразования.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="d3cfe-117">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="d3cfe-117">Effect properties</span></span>



| <span data-ttu-id="d3cfe-118">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="d3cfe-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="d3cfe-119">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d3cfe-119">Type and default value</span></span>                                                     | <span data-ttu-id="d3cfe-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d3cfe-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cfe-121">Режим</span><span class="sxs-lookup"><span data-stu-id="d3cfe-121">Mode</span></span><br/> <span data-ttu-id="d3cfe-122">D2D1 \_ морфологи \_ \_ режим Prop</span><span class="sxs-lookup"><span data-stu-id="d3cfe-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="d3cfe-123">\_Режим МОРФОЛОГИ \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="d3cfe-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="d3cfe-124">D2D1 \_ морфологи \_ Mode \_ разрушить</span><span class="sxs-lookup"><span data-stu-id="d3cfe-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="d3cfe-125">Режим морфологи.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-125">The morphology mode.</span></span> <span data-ttu-id="d3cfe-126">Доступные режимы: разрушить (сведение) и a-поздно (сиккен).</span><span class="sxs-lookup"><span data-stu-id="d3cfe-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="d3cfe-127">Дополнительные сведения см. в разделе [режимы морфологи](#morphology-modes) .</span><span class="sxs-lookup"><span data-stu-id="d3cfe-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="d3cfe-128">Ширина</span><span class="sxs-lookup"><span data-stu-id="d3cfe-128">Width</span></span><br/> <span data-ttu-id="d3cfe-129">\_Ширина D2D1 \_ морфологи \_</span><span class="sxs-lookup"><span data-stu-id="d3cfe-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="d3cfe-130">UINT</span><span class="sxs-lookup"><span data-stu-id="d3cfe-130">UINT</span></span><br/> <span data-ttu-id="d3cfe-131">1</span><span class="sxs-lookup"><span data-stu-id="d3cfe-131">1</span></span><br/>                                               | <span data-ttu-id="d3cfe-132">Размер ядра в направлении X.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="d3cfe-133">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-133">The units are in DIPs.</span></span> <span data-ttu-id="d3cfe-134">Значения должны быть в диапазоне от 1 до 100 включительно.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="d3cfe-135">Высота</span><span class="sxs-lookup"><span data-stu-id="d3cfe-135">Height</span></span><br/> <span data-ttu-id="d3cfe-136">\_Высота D2D1 \_ морфологи \_</span><span class="sxs-lookup"><span data-stu-id="d3cfe-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="d3cfe-137">UINT</span><span class="sxs-lookup"><span data-stu-id="d3cfe-137">UINT</span></span><br/> <span data-ttu-id="d3cfe-138">1</span><span class="sxs-lookup"><span data-stu-id="d3cfe-138">1</span></span><br/>                                               | <span data-ttu-id="d3cfe-139">Размер ядра в направлении Y.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="d3cfe-140">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-140">The units are in DIPs.</span></span> <span data-ttu-id="d3cfe-141">Значения должны быть в диапазоне от 1 до 100 включительно.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="d3cfe-142">Режимы морфологи</span><span class="sxs-lookup"><span data-stu-id="d3cfe-142">Morphology modes</span></span>



| <span data-ttu-id="d3cfe-143">Имя</span><span class="sxs-lookup"><span data-stu-id="d3cfe-143">Name</span></span>                           | <span data-ttu-id="d3cfe-144">Описание</span><span class="sxs-lookup"><span data-stu-id="d3cfe-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d3cfe-145">D2D1 \_ морфологи \_ Mode \_ разрушить</span><span class="sxs-lookup"><span data-stu-id="d3cfe-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="d3cfe-146">Используется максимальное значение из каждого канала RGB в ядре.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="d3cfe-147">D2D1 \_ морфологи \_ Mode \_</span><span class="sxs-lookup"><span data-stu-id="d3cfe-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="d3cfe-148">Используется минимальное значение из каждого канала RGB в ядре.</span><span class="sxs-lookup"><span data-stu-id="d3cfe-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="d3cfe-149">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="d3cfe-149">Output bitmap</span></span>

<span data-ttu-id="d3cfe-150">Для режима переводит размер битовой карты увеличивается:</span><span class="sxs-lookup"><span data-stu-id="d3cfe-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="d3cfe-151">Требование</span><span class="sxs-lookup"><span data-stu-id="d3cfe-151">Requirement</span></span> | <span data-ttu-id="d3cfe-152">Значение</span><span class="sxs-lookup"><span data-stu-id="d3cfe-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="d3cfe-153">Увеличение битовой карты вывода X =</span><span class="sxs-lookup"><span data-stu-id="d3cfe-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="d3cfe-154">INT (FLOAT (ширина) \* (dpi для пользователей)/96))</span><span class="sxs-lookup"><span data-stu-id="d3cfe-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="d3cfe-155">Увеличение битовой карты вывода Y =</span><span class="sxs-lookup"><span data-stu-id="d3cfe-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="d3cfe-156">INT (FLOAT (высота) \* (dpi пользователя)/96))</span><span class="sxs-lookup"><span data-stu-id="d3cfe-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="d3cfe-157">Для режима РАЗРУШИТЬ размер битовой карты сжимается:</span><span class="sxs-lookup"><span data-stu-id="d3cfe-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="d3cfe-158">Требование</span><span class="sxs-lookup"><span data-stu-id="d3cfe-158">Requirement</span></span> | <span data-ttu-id="d3cfe-159">Значение</span><span class="sxs-lookup"><span data-stu-id="d3cfe-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="d3cfe-160">Увеличение битовой карты вывода X =</span><span class="sxs-lookup"><span data-stu-id="d3cfe-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="d3cfe-161">INT (FLOAT (-Width) \* (dpi для пользователей)/96))</span><span class="sxs-lookup"><span data-stu-id="d3cfe-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="d3cfe-162">Увеличение битовой карты вывода Y =</span><span class="sxs-lookup"><span data-stu-id="d3cfe-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="d3cfe-163">INT (FLOAT (-Height) \* (dpi для пользователей)/96))</span><span class="sxs-lookup"><span data-stu-id="d3cfe-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d3cfe-164">Требования</span><span class="sxs-lookup"><span data-stu-id="d3cfe-164">Requirements</span></span>



| <span data-ttu-id="d3cfe-165">Требование</span><span class="sxs-lookup"><span data-stu-id="d3cfe-165">Requirement</span></span> | <span data-ttu-id="d3cfe-166">Значение</span><span class="sxs-lookup"><span data-stu-id="d3cfe-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cfe-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3cfe-167">Minimum supported client</span></span> | <span data-ttu-id="d3cfe-168">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="d3cfe-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d3cfe-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3cfe-169">Minimum supported server</span></span> | <span data-ttu-id="d3cfe-170">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="d3cfe-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d3cfe-171">Header</span><span class="sxs-lookup"><span data-stu-id="d3cfe-171">Header</span></span>                   | <span data-ttu-id="d3cfe-172">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d3cfe-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d3cfe-173">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3cfe-173">Library</span></span>                  | <span data-ttu-id="d3cfe-174">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="d3cfe-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d3cfe-175">См. также</span><span class="sxs-lookup"><span data-stu-id="d3cfe-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3cfe-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d3cfe-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

