---
description: Смена ключа
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Смена ключа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894326"
---
# <a name="key-transition"></a><span data-ttu-id="98fdc-103">Смена ключа</span><span class="sxs-lookup"><span data-stu-id="98fdc-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="98fdc-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="98fdc-104">\[Deprecated.</span></span> <span data-ttu-id="98fdc-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98fdc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="98fdc-106">При смене ключа выполняется ввод в зависимости от значения RGB, альфа-значения, оттенка или светимости.</span><span class="sxs-lookup"><span data-stu-id="98fdc-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="98fdc-107">На следующем рисунке показана смена ключа:</span><span class="sxs-lookup"><span data-stu-id="98fdc-107">The following image shows the key transition:</span></span>

![смена ключа](images/trans-key.png)

<span data-ttu-id="98fdc-109">Идентификатор класса (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="98fdc-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="98fdc-110">Имя переменной CLSID: CLSID \_ дксткэй</span><span class="sxs-lookup"><span data-stu-id="98fdc-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="98fdc-111">Понятное имя: "Дксткэй"</span><span class="sxs-lookup"><span data-stu-id="98fdc-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="98fdc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="98fdc-112">Properties</span></span>



| <span data-ttu-id="98fdc-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="98fdc-113">Property</span></span>   | <span data-ttu-id="98fdc-114">Тип</span><span class="sxs-lookup"><span data-stu-id="98fdc-114">Type</span></span>  | <span data-ttu-id="98fdc-115">Допустимый диапазон</span><span class="sxs-lookup"><span data-stu-id="98fdc-115">Valid range</span></span>           | <span data-ttu-id="98fdc-116">Описание</span><span class="sxs-lookup"><span data-stu-id="98fdc-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="98fdc-117">Применение</span><span class="sxs-lookup"><span data-stu-id="98fdc-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="98fdc-118">Оттенок</span><span class="sxs-lookup"><span data-stu-id="98fdc-118">Hue</span></span>        | <span data-ttu-id="98fdc-119">INT</span><span class="sxs-lookup"><span data-stu-id="98fdc-119">int</span></span>   | <span data-ttu-id="98fdc-120">от 0 до 360</span><span class="sxs-lookup"><span data-stu-id="98fdc-120">0–360</span></span>                 | <span data-ttu-id="98fdc-121">Значение оттенка ключа.</span><span class="sxs-lookup"><span data-stu-id="98fdc-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="98fdc-122">Оттенок</span><span class="sxs-lookup"><span data-stu-id="98fdc-122">Hue</span></span>                            |
| <span data-ttu-id="98fdc-123">Invert</span><span class="sxs-lookup"><span data-stu-id="98fdc-123">Invert</span></span>     | <span data-ttu-id="98fdc-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="98fdc-124">BOOL</span></span>  | <span data-ttu-id="98fdc-125">**False** или **true**</span><span class="sxs-lookup"><span data-stu-id="98fdc-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="98fdc-126">Логическое значение, указывающее, следует ли инвертировать операцию по умолчанию для ключа.</span><span class="sxs-lookup"><span data-stu-id="98fdc-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="98fdc-127">Если **значение равно false**, Пиксели в изображении с чрезмерной назначением становятся прозрачными по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="98fdc-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="98fdc-128">Если **значение равно true**, операция инвертирует.</span><span class="sxs-lookup"><span data-stu-id="98fdc-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="98fdc-129">Чрома, оттенок, светимость, Нонред</span><span class="sxs-lookup"><span data-stu-id="98fdc-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="98fdc-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="98fdc-130">KeyType</span></span>    | <span data-ttu-id="98fdc-131">INT</span><span class="sxs-lookup"><span data-stu-id="98fdc-131">int</span></span>   | <span data-ttu-id="98fdc-132">См. примечания</span><span class="sxs-lookup"><span data-stu-id="98fdc-132">See Remarks</span></span>           | <span data-ttu-id="98fdc-133">Указывает тип ключа.</span><span class="sxs-lookup"><span data-stu-id="98fdc-133">Specifies the type of key.</span></span> <span data-ttu-id="98fdc-134">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="98fdc-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="98fdc-135">Все</span><span class="sxs-lookup"><span data-stu-id="98fdc-135">All</span></span>                            |
| <span data-ttu-id="98fdc-136">Luminance</span><span class="sxs-lookup"><span data-stu-id="98fdc-136">Luminance</span></span>  | <span data-ttu-id="98fdc-137">INT</span><span class="sxs-lookup"><span data-stu-id="98fdc-137">int</span></span>   | <span data-ttu-id="98fdc-138">0 – 100</span><span class="sxs-lookup"><span data-stu-id="98fdc-138">0–100</span></span>                 | <span data-ttu-id="98fdc-139">Значение светимости, на которое следует подключаться.</span><span class="sxs-lookup"><span data-stu-id="98fdc-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="98fdc-140">Luminance</span><span class="sxs-lookup"><span data-stu-id="98fdc-140">Luminance</span></span>                      |
| <span data-ttu-id="98fdc-141">RGB</span><span class="sxs-lookup"><span data-stu-id="98fdc-141">RGB</span></span>        | <span data-ttu-id="98fdc-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="98fdc-142">DWORD</span></span> | <span data-ttu-id="98fdc-143">0x0 — 0xFFFFFF</span><span class="sxs-lookup"><span data-stu-id="98fdc-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="98fdc-144">Цвет ключа.</span><span class="sxs-lookup"><span data-stu-id="98fdc-144">The color on which to key.</span></span> <span data-ttu-id="98fdc-145">Значение представляет собой шестнадцатеричное число в формате 0x *RRGGBB*, где *RR* является красным значением, *GG* — зеленым значением, а *BB* — синим.</span><span class="sxs-lookup"><span data-stu-id="98fdc-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="98fdc-146">(Чисто красный, зеленый и синий — 0xFF0000, 0x00FF00 и 0x0000FF соответственно.)</span><span class="sxs-lookup"><span data-stu-id="98fdc-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="98fdc-147">чрома</span><span class="sxs-lookup"><span data-stu-id="98fdc-147">Chroma</span></span>                         |
| <span data-ttu-id="98fdc-148">Сходство</span><span class="sxs-lookup"><span data-stu-id="98fdc-148">Similarity</span></span> | <span data-ttu-id="98fdc-149">INT</span><span class="sxs-lookup"><span data-stu-id="98fdc-149">int</span></span>   | <span data-ttu-id="98fdc-150">0 – 100</span><span class="sxs-lookup"><span data-stu-id="98fdc-150">0–100</span></span>                 | <span data-ttu-id="98fdc-151">Диапазон цветовых данных, которые становятся прозрачными.</span><span class="sxs-lookup"><span data-stu-id="98fdc-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="98fdc-152">При более высоких значениях более широкий диапазон похожих цветов является прозрачным.</span><span class="sxs-lookup"><span data-stu-id="98fdc-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="98fdc-153">Чрома, Нонред</span><span class="sxs-lookup"><span data-stu-id="98fdc-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="98fdc-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98fdc-154">Remarks</span></span>

<span data-ttu-id="98fdc-155">Тип выполняемого ключа зависит от значения свойства **KeyType** , которое должно быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="98fdc-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="98fdc-156">Значение</span><span class="sxs-lookup"><span data-stu-id="98fdc-156">Value</span></span> | <span data-ttu-id="98fdc-157">Перечисление</span><span class="sxs-lookup"><span data-stu-id="98fdc-157">Enumeration</span></span>       | <span data-ttu-id="98fdc-158">Описание</span><span class="sxs-lookup"><span data-stu-id="98fdc-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="98fdc-159">0</span><span class="sxs-lookup"><span data-stu-id="98fdc-159">0</span></span>     | <span data-ttu-id="98fdc-160">ДКСТКЭЙ \_ RGB</span><span class="sxs-lookup"><span data-stu-id="98fdc-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="98fdc-161">Ключ чрома (значение ключа по RGB).</span><span class="sxs-lookup"><span data-stu-id="98fdc-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="98fdc-162">1</span><span class="sxs-lookup"><span data-stu-id="98fdc-162">1</span></span>     | <span data-ttu-id="98fdc-163">ДКСТКЭЙ \_ нонред</span><span class="sxs-lookup"><span data-stu-id="98fdc-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="98fdc-164">Ключ нонред.</span><span class="sxs-lookup"><span data-stu-id="98fdc-164">Nonred key.</span></span> <span data-ttu-id="98fdc-165">(Делает прозрачными синие и зеленые области.)</span><span class="sxs-lookup"><span data-stu-id="98fdc-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="98fdc-166">2</span><span class="sxs-lookup"><span data-stu-id="98fdc-166">2</span></span>     | <span data-ttu-id="98fdc-167">\_светимость дксткэй</span><span class="sxs-lookup"><span data-stu-id="98fdc-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="98fdc-168">Ключ освещенности.</span><span class="sxs-lookup"><span data-stu-id="98fdc-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="98fdc-169">3</span><span class="sxs-lookup"><span data-stu-id="98fdc-169">3</span></span>     | <span data-ttu-id="98fdc-170">ДКСТКЭЙ \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="98fdc-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="98fdc-171">Ключ по значению альфа.</span><span class="sxs-lookup"><span data-stu-id="98fdc-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="98fdc-172">4</span><span class="sxs-lookup"><span data-stu-id="98fdc-172">4</span></span>     | <span data-ttu-id="98fdc-173">оттенок ДКСТКЭЙ \_</span><span class="sxs-lookup"><span data-stu-id="98fdc-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="98fdc-174">Ключ с оттенокм.</span><span class="sxs-lookup"><span data-stu-id="98fdc-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="98fdc-175">Тип ключа по умолчанию — ДКСТКЭЙ \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="98fdc-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



