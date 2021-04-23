---
title: Эффекты RGB-оттенков
description: Преобразует изображение RGB в цветовые пространства HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415365"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="018a3-103">Эффекты RGB-оттенков</span><span class="sxs-lookup"><span data-stu-id="018a3-103">RGB-to-hue effect</span></span>

<span data-ttu-id="018a3-104">Преобразует изображение RGB в цветовые пространства HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение).</span><span class="sxs-lookup"><span data-stu-id="018a3-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="018a3-105">HSL и HSV — это две различные модели для представления цвета RGB в виде цилиндров цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="018a3-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="018a3-106">Они полезны, так как они позволяют понять цвет с помощью более интуитивно понятных концепций, таких как оттенок и интенсивность, а также сочетания красного, зеленого и синего значений.</span><span class="sxs-lookup"><span data-stu-id="018a3-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="018a3-107">Этот результат нормализует выходные данные (оттенок, значение насыщенности для HSV или оттенка, насыщенность, освещение для HSL) до диапазона \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="018a3-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="018a3-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1RgbToHue.</span><span class="sxs-lookup"><span data-stu-id="018a3-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="018a3-109">Чтобы изменить поведение этого действия, используйте [эффекты оттенок для RGB](hue-to-rgb-effect.md).</span><span class="sxs-lookup"><span data-stu-id="018a3-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="018a3-110">Образец кода</span><span class="sxs-lookup"><span data-stu-id="018a3-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="018a3-111">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="018a3-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="018a3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="018a3-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="018a3-113">См. также</span><span class="sxs-lookup"><span data-stu-id="018a3-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="018a3-114">Пример кода</span><span class="sxs-lookup"><span data-stu-id="018a3-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="018a3-115">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="018a3-115">Effect properties</span></span>

<span data-ttu-id="018a3-116">Свойства для эффектов контрастности определяются перечислением [**D2D1 \_ ргбтохуе \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .</span><span class="sxs-lookup"><span data-stu-id="018a3-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="018a3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="018a3-117">Requirements</span></span>



| <span data-ttu-id="018a3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="018a3-118">Requirement</span></span> | <span data-ttu-id="018a3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="018a3-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="018a3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="018a3-120">Minimum supported client</span></span> | <span data-ttu-id="018a3-121">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="018a3-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="018a3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="018a3-122">Minimum supported server</span></span> | <span data-ttu-id="018a3-123">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="018a3-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="018a3-124">Header</span><span class="sxs-lookup"><span data-stu-id="018a3-124">Header</span></span>                   | <span data-ttu-id="018a3-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="018a3-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="018a3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="018a3-126">Library</span></span>                  | <span data-ttu-id="018a3-127">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="018a3-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="018a3-128">См. также</span><span class="sxs-lookup"><span data-stu-id="018a3-128">Related topics</span></span>

* [<span data-ttu-id="018a3-129">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="018a3-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
