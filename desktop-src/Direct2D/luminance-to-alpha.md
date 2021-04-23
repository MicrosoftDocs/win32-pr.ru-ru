---
title: Воздействие светимости на альфа
description: Используйте воздействие «светимость на альфа», чтобы установить альфа-канал на светимость изображения и задать для цветовых каналов значение 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- воздействие светимости на альфа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104556321"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="15c62-104">Воздействие светимости на альфа</span><span class="sxs-lookup"><span data-stu-id="15c62-104">Luminance to alpha effect</span></span>

<span data-ttu-id="15c62-105">Используйте воздействие «светимость на альфа», чтобы установить альфа-канал на светимость изображения и задать для цветовых каналов значение 0.</span><span class="sxs-lookup"><span data-stu-id="15c62-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="15c62-106">Вывод этого результата можно использовать для создания полупрозрачного наложения на основе яркости входного изображения.</span><span class="sxs-lookup"><span data-stu-id="15c62-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="15c62-107">Его также можно использовать для создания маски изображения.</span><span class="sxs-lookup"><span data-stu-id="15c62-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="15c62-108">У этого действия нет свойств.</span><span class="sxs-lookup"><span data-stu-id="15c62-108">This effect has no properties.</span></span>

 

<span data-ttu-id="15c62-109">Идентификатором CLSID для этого действия является CLSID \_ D2D1LuminanceToAlpha.</span><span class="sxs-lookup"><span data-stu-id="15c62-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="15c62-110">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="15c62-110">Example image</span></span>

<span data-ttu-id="15c62-111">В этом примере показаны выходные данные светимости в альфа-эффекты, совмещенные на белой поверхности для отображения прозрачности.</span><span class="sxs-lookup"><span data-stu-id="15c62-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="15c62-112">До</span><span class="sxs-lookup"><span data-stu-id="15c62-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)        |
| <span data-ttu-id="15c62-114">После</span><span class="sxs-lookup"><span data-stu-id="15c62-114">After</span></span>                                                             |
| ![изображение после преобразования.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="15c62-116">Этот результат устанавливает в качестве альфа-канала выходных данных светимость входного изображения, используя эту матрицу цветов.</span><span class="sxs-lookup"><span data-stu-id="15c62-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![Цветовая матрица, используемая для установки альфа-канала.](images/luminance-to-alpha-math1.png)

<span data-ttu-id="15c62-118">Этот результат использует и выводит предварительно умноженные альфа-изображения.</span><span class="sxs-lookup"><span data-stu-id="15c62-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="15c62-119">Этот результат не будет работать с прямыми альфа-изображениями, если они не полностью непрозрачны.</span><span class="sxs-lookup"><span data-stu-id="15c62-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="15c62-120">Поскольку изображения хранятся в формате с гамма-компенсацией, перед вычислением светимости для изображения необходимо сначала выполнить инверсную гамму-коррекцию, чтобы получить значения True Color для изображения.</span><span class="sxs-lookup"><span data-stu-id="15c62-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="15c62-121">Так как изображения обычно хранятся в 2,2 гаммы, можно использовать гамма-пересылку с экспонентой (1/2.2), а затем использовать выходные данные этого результата.</span><span class="sxs-lookup"><span data-stu-id="15c62-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15c62-122">Требования</span><span class="sxs-lookup"><span data-stu-id="15c62-122">Requirements</span></span>



| <span data-ttu-id="15c62-123">Требование</span><span class="sxs-lookup"><span data-stu-id="15c62-123">Requirement</span></span> | <span data-ttu-id="15c62-124">Значение</span><span class="sxs-lookup"><span data-stu-id="15c62-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15c62-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15c62-125">Minimum supported client</span></span> | <span data-ttu-id="15c62-126">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="15c62-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="15c62-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15c62-127">Minimum supported server</span></span> | <span data-ttu-id="15c62-128">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="15c62-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="15c62-129">Header</span><span class="sxs-lookup"><span data-stu-id="15c62-129">Header</span></span>                   | <span data-ttu-id="15c62-130">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="15c62-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="15c62-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="15c62-131">Library</span></span>                  | <span data-ttu-id="15c62-132">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="15c62-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="15c62-133">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="15c62-133">Output bitmap</span></span>

<span data-ttu-id="15c62-134">Выходные данные имеют тот же размер, что и входной образ.</span><span class="sxs-lookup"><span data-stu-id="15c62-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15c62-135">См. также</span><span class="sxs-lookup"><span data-stu-id="15c62-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15c62-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="15c62-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
