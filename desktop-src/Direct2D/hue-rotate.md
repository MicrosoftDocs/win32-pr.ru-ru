---
title: Ротататионный тон, результат
description: Используйте параметр цветовой тон, чтобы изменить оттенок изображения, применив цветовую матрицу на основе угла поворота.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- ротататионный тон, результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104553337"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="e2fc4-104">Ротататионный тон, результат</span><span class="sxs-lookup"><span data-stu-id="e2fc4-104">Hue rotatation effect</span></span>

<span data-ttu-id="e2fc4-105">Используйте параметр цветовой тон, чтобы изменить оттенок изображения, применив цветовую матрицу на основе угла поворота.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="e2fc4-106">Идентификатором CLSID для этого действия является CLSID \_ D2D1HueRotation.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="e2fc4-107">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="e2fc4-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e2fc4-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="e2fc4-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e2fc4-109">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="e2fc4-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e2fc4-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e2fc4-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e2fc4-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e2fc4-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e2fc4-112">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="e2fc4-112">Example image</span></span>

<span data-ttu-id="e2fc4-113">В примере ниже показано, как повлиять на входные и выходные изображения оттенка, используя угол поворота в 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="e2fc4-114">До</span><span class="sxs-lookup"><span data-stu-id="e2fc4-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![изображение перед результатом.](images/default-before.jpg)   |
| <span data-ttu-id="e2fc4-116">После</span><span class="sxs-lookup"><span data-stu-id="e2fc4-116">After</span></span>                                                        |
| ![изображение после преобразования.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="e2fc4-118">Этот результат вычисляет матрицу цветов на основе угла поворота (*?*), указанного с помощью \_ \_ \_ свойства Angle D2D1 хуеротатион.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="e2fc4-119">Ниже приведены матричные уравнения.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-119">Here are the matrix equations.</span></span>

![Вычисление поворота оттенков](images/hue-formula.png)

<span data-ttu-id="e2fc4-121">Созданная матрица зависит только от угла поворота.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="e2fc4-122">Если требуется определенная матрица, можно использовать [цветовую матрицу](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="e2fc4-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="e2fc4-123">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="e2fc4-123">Effect properties</span></span>



| <span data-ttu-id="e2fc4-124">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="e2fc4-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="e2fc4-125">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e2fc4-125">Type and default value</span></span>           | <span data-ttu-id="e2fc4-126">Описание</span><span class="sxs-lookup"><span data-stu-id="e2fc4-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="e2fc4-127">Angle</span><span class="sxs-lookup"><span data-stu-id="e2fc4-127">Angle</span></span><br/> <span data-ttu-id="e2fc4-128">D2D1 \_ хуеротатион \_ , \_ угол</span><span class="sxs-lookup"><span data-stu-id="e2fc4-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="e2fc4-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e2fc4-129">FLOAT</span></span><br/> <span data-ttu-id="e2fc4-130">указано</span><span class="sxs-lookup"><span data-stu-id="e2fc4-130">0.0f</span></span><br/> | <span data-ttu-id="e2fc4-131">Угол поворота оттенка в градусах.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="e2fc4-132">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="e2fc4-132">Output bitmap</span></span>

<span data-ttu-id="e2fc4-133">Размер выходного растрового изображения совпадает с размером входного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="e2fc4-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fc4-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e2fc4-134">Requirements</span></span>



| <span data-ttu-id="e2fc4-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e2fc4-135">Requirement</span></span> | <span data-ttu-id="e2fc4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e2fc4-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fc4-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2fc4-137">Minimum supported client</span></span> | <span data-ttu-id="e2fc4-138">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="e2fc4-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e2fc4-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2fc4-139">Minimum supported server</span></span> | <span data-ttu-id="e2fc4-140">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="e2fc4-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e2fc4-141">Header</span><span class="sxs-lookup"><span data-stu-id="e2fc4-141">Header</span></span>                   | <span data-ttu-id="e2fc4-142">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e2fc4-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e2fc4-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e2fc4-143">Library</span></span>                  | <span data-ttu-id="e2fc4-144">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="e2fc4-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e2fc4-145">См. также</span><span class="sxs-lookup"><span data-stu-id="e2fc4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2fc4-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e2fc4-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

