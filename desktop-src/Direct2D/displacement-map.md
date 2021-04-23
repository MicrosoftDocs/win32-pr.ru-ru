---
title: Результат распределения искривлений
description: Используйте эффекты распределения смещения, чтобы не размещать пикселы входного изображения по значениям интенсивности второго входного изображения.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- результат распределения искривлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135186"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="cfb95-104">Результат распределения искривлений</span><span class="sxs-lookup"><span data-stu-id="cfb95-104">Displacement map effect</span></span>

<span data-ttu-id="cfb95-105">Используйте эффекты распределения смещения, чтобы не размещать пикселы входного изображения по значениям интенсивности второго входного изображения.</span><span class="sxs-lookup"><span data-stu-id="cfb95-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="cfb95-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1DisplacementMap.</span><span class="sxs-lookup"><span data-stu-id="cfb95-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="cfb95-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="cfb95-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="cfb95-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="cfb95-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="cfb95-109">Цветовые каналы</span><span class="sxs-lookup"><span data-stu-id="cfb95-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="cfb95-110">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="cfb95-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="cfb95-111">Требования</span><span class="sxs-lookup"><span data-stu-id="cfb95-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cfb95-112">См. также</span><span class="sxs-lookup"><span data-stu-id="cfb95-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="cfb95-113">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="cfb95-113">Example image</span></span>



| <span data-ttu-id="cfb95-114">До</span><span class="sxs-lookup"><span data-stu-id="cfb95-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)       |
| <span data-ttu-id="cfb95-116">После</span><span class="sxs-lookup"><span data-stu-id="cfb95-116">After</span></span>                                                            |
| ![изображение после преобразования.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="cfb95-118">Расположение пикселей в выходных данных определяется с помощью следующей формулы:</span><span class="sxs-lookup"><span data-stu-id="cfb95-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="cfb95-119">C "(x, y) = C (x + Scale \* (ксчаннелселектор (смещение смещения (x, y))-0,5), y + Scale \* (Ичаннелселектор (битовая карта смещения (x, y))-0,5))</span><span class="sxs-lookup"><span data-stu-id="cfb95-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="cfb95-120">Где:</span><span class="sxs-lookup"><span data-stu-id="cfb95-120">Where:</span></span><dl> <span data-ttu-id="cfb95-121">*C (x, y)* является выходным пикселем в (x, y).</span><span class="sxs-lookup"><span data-stu-id="cfb95-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="cfb95-122">*C (x, y)* — это входной пиксель в (x, y).</span><span class="sxs-lookup"><span data-stu-id="cfb95-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="cfb95-123">*Битовая карта смещения (x, y)* — это интенсивность пикселя смещения в указанных координатах</span><span class="sxs-lookup"><span data-stu-id="cfb95-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="cfb95-124">*Ксчаннелселекторет* интенсивность выбранного канала RGBA из битовой карты смещения, которая вымещает изображение ввода в направлении X.</span><span class="sxs-lookup"><span data-stu-id="cfb95-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="cfb95-125">*Ичаннелселекторет* интенсивность выбранного канала RGBA из битовой карты смещения, которая перемещает входной рисунок в направлении Y.</span><span class="sxs-lookup"><span data-stu-id="cfb95-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="cfb95-126">Этот результат позволяет повторно выполнить выборку входного изображения в соответствии со свойством Scale и интенсивностью изображения смещения.</span><span class="sxs-lookup"><span data-stu-id="cfb95-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="cfb95-127">Он использует интерполяцию билинейной, если выборка между пикселями во входном изображении.</span><span class="sxs-lookup"><span data-stu-id="cfb95-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="cfb95-128">Этот результат работает с прямыми и предварительно умноженными альфа-образами.</span><span class="sxs-lookup"><span data-stu-id="cfb95-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="cfb95-129">Формат вывода альфа совпадает с форматом ввода.</span><span class="sxs-lookup"><span data-stu-id="cfb95-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="cfb95-130">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="cfb95-130">Effect properties</span></span>



| <span data-ttu-id="cfb95-131">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="cfb95-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="cfb95-132">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cfb95-132">Type and default value</span></span>                                                   | <span data-ttu-id="cfb95-133">Описание</span><span class="sxs-lookup"><span data-stu-id="cfb95-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb95-134">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="cfb95-134">Scale</span></span><br/> <span data-ttu-id="cfb95-135">D2D1 \_ дисплацементмап \_ prop \_ Scale</span><span class="sxs-lookup"><span data-stu-id="cfb95-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="cfb95-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="cfb95-136">FLOAT</span></span><br/> <span data-ttu-id="cfb95-137">указано</span><span class="sxs-lookup"><span data-stu-id="cfb95-137">0.0f</span></span><br/>                                         | <span data-ttu-id="cfb95-138">Умножает интенсивность выбранного канала от изображения смещения.</span><span class="sxs-lookup"><span data-stu-id="cfb95-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="cfb95-139">Чем выше значение этого свойства, тем больше будет расположить Пиксели.</span><span class="sxs-lookup"><span data-stu-id="cfb95-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="cfb95-140">ксчаннелселект</span><span class="sxs-lookup"><span data-stu-id="cfb95-140">XChannelSelect</span></span><br/> <span data-ttu-id="cfb95-141">D2D1 \_ дисплацементмап \_ prop \_ X \_ \_ Выбор канала</span><span class="sxs-lookup"><span data-stu-id="cfb95-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="cfb95-142">\_Выбор канала \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="cfb95-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="cfb95-143">\_Селектор каналов \_ D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="cfb95-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="cfb95-144">Этот результат извлекает интенсивность из этого канала цвета и использует его для пространственного размещения изображения в направлении X.</span><span class="sxs-lookup"><span data-stu-id="cfb95-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="cfb95-145">Дополнительные сведения см. в разделе [цветовые каналы](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="cfb95-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="cfb95-146">ичаннелселект</span><span class="sxs-lookup"><span data-stu-id="cfb95-146">YChannelSelect</span></span><br/> <span data-ttu-id="cfb95-147">\_SELECT D2D1 \_ дисплацементмап \_ prop \_ Y \_</span><span class="sxs-lookup"><span data-stu-id="cfb95-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="cfb95-148">\_Выбор канала \_ D2D1</span><span class="sxs-lookup"><span data-stu-id="cfb95-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="cfb95-149">\_Селектор каналов \_ D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="cfb95-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="cfb95-150">Этот результат извлекает интенсивность из этого канала цвета и использует его для пространственного размещения изображения в направлении Y.</span><span class="sxs-lookup"><span data-stu-id="cfb95-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="cfb95-151">Дополнительные сведения см. в разделе [цветовые каналы](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="cfb95-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="cfb95-152">Цветовые каналы</span><span class="sxs-lookup"><span data-stu-id="cfb95-152">Color channels</span></span>



| <span data-ttu-id="cfb95-153">Перечисление</span><span class="sxs-lookup"><span data-stu-id="cfb95-153">Enumeration</span></span>                | <span data-ttu-id="cfb95-154">Описание</span><span class="sxs-lookup"><span data-stu-id="cfb95-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="cfb95-155">\_Выбор канала \_ D2D1 \_ R</span><span class="sxs-lookup"><span data-stu-id="cfb95-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="cfb95-156">Этот результат извлекает интенсивность выходных данных из красного канала.</span><span class="sxs-lookup"><span data-stu-id="cfb95-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="cfb95-157">\_Селектор канала \_ D2D1 \_ G</span><span class="sxs-lookup"><span data-stu-id="cfb95-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="cfb95-158">Этот результат извлекает интенсивность выходных данных из зеленого канала.</span><span class="sxs-lookup"><span data-stu-id="cfb95-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="cfb95-159">\_Селектор каналов \_ D2D1 \_ B</span><span class="sxs-lookup"><span data-stu-id="cfb95-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="cfb95-160">Этот результат извлекает интенсивность выходных данных из синего канала.</span><span class="sxs-lookup"><span data-stu-id="cfb95-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="cfb95-161">\_Селектор каналов \_ D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="cfb95-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="cfb95-162">Этот результат извлекает интенсивность выходных данных из альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="cfb95-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="cfb95-163">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="cfb95-163">Output Bitmap</span></span>

<span data-ttu-id="cfb95-164">Вы можете определить максимальный размер выходного точечного рисунка со следующими уравнениями:</span><span class="sxs-lookup"><span data-stu-id="cfb95-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="cfb95-165">Выводить точечный рисунок?</span><span class="sxs-lookup"><span data-stu-id="cfb95-165">Output Bitmap?</span></span> <span data-ttu-id="cfb95-166">ПКС = (размер входного точечного рисунка?) ( DIP) + Scale) \* (dpi пользователя/96)</span><span class="sxs-lookup"><span data-stu-id="cfb95-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="cfb95-167">Выходное битовое изображение<sub>y</sub> пикселей = (размер входного рисунка<sub>y</sub>(DIP) + масштаб) \* (dpi пользователя/96)</span><span class="sxs-lookup"><span data-stu-id="cfb95-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb95-168">Требования</span><span class="sxs-lookup"><span data-stu-id="cfb95-168">Requirements</span></span>



| <span data-ttu-id="cfb95-169">Требование</span><span class="sxs-lookup"><span data-stu-id="cfb95-169">Requirement</span></span> | <span data-ttu-id="cfb95-170">Значение</span><span class="sxs-lookup"><span data-stu-id="cfb95-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb95-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfb95-171">Minimum supported client</span></span> | <span data-ttu-id="cfb95-172">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="cfb95-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cfb95-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfb95-173">Minimum supported server</span></span> | <span data-ttu-id="cfb95-174">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="cfb95-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="cfb95-175">Header</span><span class="sxs-lookup"><span data-stu-id="cfb95-175">Header</span></span>                   | <span data-ttu-id="cfb95-176">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="cfb95-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="cfb95-177">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cfb95-177">Library</span></span>                  | <span data-ttu-id="cfb95-178">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="cfb95-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="cfb95-179">См. также</span><span class="sxs-lookup"><span data-stu-id="cfb95-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfb95-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="cfb95-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

