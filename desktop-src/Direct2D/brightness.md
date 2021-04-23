---
title: Эффекты яркости
description: Используйте эффекты яркости для управления яркостью изображения.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- эффекты яркости
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104567803"
---
# <a name="brightness-effect"></a><span data-ttu-id="6f1cd-104">Эффекты яркости</span><span class="sxs-lookup"><span data-stu-id="6f1cd-104">Brightness effect</span></span>

<span data-ttu-id="6f1cd-105">Используйте эффекты яркости для управления яркостью изображения.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="6f1cd-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1Brightness.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="6f1cd-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="6f1cd-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="6f1cd-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="6f1cd-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6f1cd-109">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="6f1cd-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="6f1cd-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6f1cd-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6f1cd-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6f1cd-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6f1cd-112">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="6f1cd-112">Example image</span></span>



| <span data-ttu-id="6f1cd-113">До</span><span class="sxs-lookup"><span data-stu-id="6f1cd-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)  |
| <span data-ttu-id="6f1cd-115">После</span><span class="sxs-lookup"><span data-stu-id="6f1cd-115">After</span></span>                                                       |
| ![изображение после преобразования.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="6f1cd-117">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="6f1cd-117">Effect properties</span></span>



| <span data-ttu-id="6f1cd-118">Отображаемое имя свойства</span><span class="sxs-lookup"><span data-stu-id="6f1cd-118">Property Display Name</span></span>                                                 | <span data-ttu-id="6f1cd-119">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6f1cd-119">Type and default value</span></span>                              | <span data-ttu-id="6f1cd-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6f1cd-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1cd-121">вхитепоинт</span><span class="sxs-lookup"><span data-stu-id="6f1cd-121">WhitePoint</span></span><br/> <span data-ttu-id="6f1cd-122">\_ \_ \_ Белая \_ точка prop для D2D1 яркости</span><span class="sxs-lookup"><span data-stu-id="6f1cd-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="6f1cd-123">D2D1 \_ vector \_</span><span class="sxs-lookup"><span data-stu-id="6f1cd-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="6f1cd-124">{1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="6f1cd-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="6f1cd-125">Верхняя часть кривой перемещения яркости.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="6f1cd-126">Белая точка настраивает внешний вид более ярких частей изображения.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="6f1cd-127">Это свойство относится как к значению x, так и к значению y в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="6f1cd-128">Каждое из значений этого свойства находится в диапазоне от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="6f1cd-129">блаккпоинт</span><span class="sxs-lookup"><span data-stu-id="6f1cd-129">BlackPoint</span></span><br/> <span data-ttu-id="6f1cd-130">\_ \_ \_ Черная \_ точка Prop яркости D2D1</span><span class="sxs-lookup"><span data-stu-id="6f1cd-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="6f1cd-131">D2D1 \_ vector \_</span><span class="sxs-lookup"><span data-stu-id="6f1cd-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="6f1cd-132">{0.0 f, 0,0 f}</span><span class="sxs-lookup"><span data-stu-id="6f1cd-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="6f1cd-133">Нижняя часть кривой перемещения яркости.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="6f1cd-134">Черная точка настраивает внешний вид более темных частей изображения.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="6f1cd-135">Это свойство относится как к значению x, так и к значению y в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="6f1cd-136">Каждое из значений этого свойства находится в диапазоне от 0 до 1 включительно.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="6f1cd-137">Этот результат использует указанные белые и черные точки для создания функции перемещения, используемой для корректировки точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="6f1cd-138">В следующем уравнении описывается функция пересылки.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="6f1cd-139">Входные интенситиес определяются между 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-139">The input intensities are defined between 0 and 1.</span></span>

![алгоритм яркости](images/brightness-formula1.png)

<span data-ttu-id="6f1cd-141">Алгоритм эффектов реализует уравнение, создающее функцию пересылки.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="6f1cd-142">Мы используем эту функцию для корректировки пикселов изображения.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="6f1cd-143">Значения x и y черной точки и белой точки являются координатами в двух измерениях, Соединенных для преобразования.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="6f1cd-144">Каждая часть окончательного выражения вывода:</span><span class="sxs-lookup"><span data-stu-id="6f1cd-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="6f1cd-145">Преобразует данные изображения из линейного пространства в нелинейное, используя это уравнение:</span><span class="sxs-lookup"><span data-stu-id="6f1cd-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![вспомогательная функция 1](images/brightness-formula2.png)

2.  <span data-ttu-id="6f1cd-147">Корректирует изображение в соответствии со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="6f1cd-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="6f1cd-148">*входные данные* — это значения интенсивности точечного рисунка от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="6f1cd-149">*Белая пт (x, y)* расположение кривой преобразования для более светлой пиксельной интенситиес.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="6f1cd-150">*Черный PT (x, y)* — это расположение кривой преобразования для интенситиес пикселов DIMM.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="6f1cd-151">Преобразует данные изображения обратно в линейное пространство с помощью этого уравнения:</span><span class="sxs-lookup"><span data-stu-id="6f1cd-151">Converts the image data back to linear space using this equation:</span></span> ![вспомогательная функция 2](images/brightness-formula3.png)

<span data-ttu-id="6f1cd-153">Здесь показаны окончательное выходное уравнение и части компонентов.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-153">The final output equation and the component parts are shown here.</span></span>

![полные вычисления для настройки яркости](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="6f1cd-155">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="6f1cd-155">Output bitmap</span></span>

<span data-ttu-id="6f1cd-156">Размер выходного растрового изображения совпадает с размером входного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="6f1cd-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1cd-157">Требования</span><span class="sxs-lookup"><span data-stu-id="6f1cd-157">Requirements</span></span>



| <span data-ttu-id="6f1cd-158">Требование</span><span class="sxs-lookup"><span data-stu-id="6f1cd-158">Requirement</span></span> | <span data-ttu-id="6f1cd-159">Значение</span><span class="sxs-lookup"><span data-stu-id="6f1cd-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1cd-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f1cd-160">Minimum supported client</span></span> | <span data-ttu-id="6f1cd-161">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="6f1cd-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6f1cd-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f1cd-162">Minimum supported server</span></span> | <span data-ttu-id="6f1cd-163">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="6f1cd-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6f1cd-164">Header</span><span class="sxs-lookup"><span data-stu-id="6f1cd-164">Header</span></span>                   | <span data-ttu-id="6f1cd-165">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6f1cd-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6f1cd-166">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f1cd-166">Library</span></span>                  | <span data-ttu-id="6f1cd-167">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="6f1cd-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6f1cd-168">См. также</span><span class="sxs-lookup"><span data-stu-id="6f1cd-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f1cd-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6f1cd-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

