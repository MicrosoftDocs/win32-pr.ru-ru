---
title: Результат кадрирования
description: Используйте эффекты кадрирования для вывода заданной области изображения.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- результат кадрирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891885"
---
# <a name="crop-effect"></a><span data-ttu-id="5fd52-104">Результат кадрирования</span><span class="sxs-lookup"><span data-stu-id="5fd52-104">Crop effect</span></span>

<span data-ttu-id="5fd52-105">Используйте эффекты кадрирования для вывода заданной области изображения.</span><span class="sxs-lookup"><span data-stu-id="5fd52-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="5fd52-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1Crop.</span><span class="sxs-lookup"><span data-stu-id="5fd52-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="5fd52-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="5fd52-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="5fd52-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="5fd52-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5fd52-109">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="5fd52-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="5fd52-110">Требования</span><span class="sxs-lookup"><span data-stu-id="5fd52-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5fd52-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5fd52-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5fd52-112">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="5fd52-112">Example image</span></span>



| <span data-ttu-id="5fd52-113">До</span><span class="sxs-lookup"><span data-stu-id="5fd52-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg) |
| <span data-ttu-id="5fd52-115">После</span><span class="sxs-lookup"><span data-stu-id="5fd52-115">After</span></span>                                                      |
| ![изображение после преобразования.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="5fd52-117">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="5fd52-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5fd52-118">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="5fd52-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="5fd52-119">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5fd52-119">Type and default value</span></span></th>
<th><span data-ttu-id="5fd52-120">Описание</span><span class="sxs-lookup"><span data-stu-id="5fd52-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5fd52-121">Rect</span><span class="sxs-lookup"><span data-stu-id="5fd52-121">Rect</span></span><br/></td>
<td><span data-ttu-id="5fd52-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="5fd52-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="5fd52-123">Регион, который необходимо обрезать, заданный в виде вектора в форме (слева, сверху, по ширине, по высоте).</span><span class="sxs-lookup"><span data-stu-id="5fd52-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5fd52-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="5fd52-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="5fd52-125">{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="5fd52-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="5fd52-126">Единицы измерения — DIP.</span><span class="sxs-lookup"><span data-stu-id="5fd52-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="5fd52-127">Параметр rect будет обрезан, если он пересекает границы границ входного изображения.</span><span class="sxs-lookup"><span data-stu-id="5fd52-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5fd52-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="5fd52-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="5fd52-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="5fd52-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="5fd52-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="5fd52-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="5fd52-131">D2D1_BORDER_MODE_SOFT: если прямоугольник кадрирования попадает на координаты в виде дробной части пикселя, то этот результат применяет сглаживание, что приводит к мягкому пограничным углу.</span><span class="sxs-lookup"><span data-stu-id="5fd52-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="5fd52-132">D2D1_BORDER_MODE_HARD: если прямоугольник кадрирования попадает на координаты в виде дробной части пикселя, то результат будет резким, что приводит к жесткой границе.</span><span class="sxs-lookup"><span data-stu-id="5fd52-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="5fd52-133">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="5fd52-133">Output bitmap</span></span>

<span data-ttu-id="5fd52-134">Результатом этого действия является размер свойства Rect.</span><span class="sxs-lookup"><span data-stu-id="5fd52-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="5fd52-135">Длина и ширина являются вычисляемыми</span><span class="sxs-lookup"><span data-stu-id="5fd52-135">The length and width are calc</span></span>

<span data-ttu-id="5fd52-136">улатед с помощью уравнений здесь:</span><span class="sxs-lookup"><span data-stu-id="5fd52-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="5fd52-137">Длина выходных данных в пикселях = (Rect. Right-Rect. Left) \* (dpi пользователя/96)</span><span class="sxs-lookup"><span data-stu-id="5fd52-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="5fd52-138">Высота выходных данных в пикселях = (Rect. Bottom-Rect.Top) \* (dpi пользователя/96)</span><span class="sxs-lookup"><span data-stu-id="5fd52-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="5fd52-139">Требования</span><span class="sxs-lookup"><span data-stu-id="5fd52-139">Requirements</span></span>



| <span data-ttu-id="5fd52-140">Требование</span><span class="sxs-lookup"><span data-stu-id="5fd52-140">Requirement</span></span> | <span data-ttu-id="5fd52-141">Значение</span><span class="sxs-lookup"><span data-stu-id="5fd52-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd52-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fd52-142">Minimum supported client</span></span> | <span data-ttu-id="5fd52-143">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="5fd52-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5fd52-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fd52-144">Minimum supported server</span></span> | <span data-ttu-id="5fd52-145">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="5fd52-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5fd52-146">Header</span><span class="sxs-lookup"><span data-stu-id="5fd52-146">Header</span></span>                   | <span data-ttu-id="5fd52-147">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="5fd52-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="5fd52-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5fd52-148">Library</span></span>                  | <span data-ttu-id="5fd52-149">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="5fd52-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="5fd52-150">См. также</span><span class="sxs-lookup"><span data-stu-id="5fd52-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fd52-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="5fd52-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

