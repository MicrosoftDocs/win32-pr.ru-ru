---
title: Эффекты оттенка по RGB
description: Преобразует изображение HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение) в цветовое пространство RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988585"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="a9107-103">Эффекты оттенка по RGB</span><span class="sxs-lookup"><span data-stu-id="a9107-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="a9107-104">Преобразует изображение HSL (оттенок, насыщенность, освещение) или HSV (оттенок, насыщенность, значение) в цветовое пространство RGB.</span><span class="sxs-lookup"><span data-stu-id="a9107-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="a9107-105">HSL и HSV — это две различные модели для представления цвета RGB в виде цилиндров цветового пространства.</span><span class="sxs-lookup"><span data-stu-id="a9107-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="a9107-106">Они полезны, так как они позволяют понять цвет с помощью более интуитивно понятных концепций, таких как оттенок и интенсивность, а также сочетания красного, зеленого и синего значений.</span><span class="sxs-lookup"><span data-stu-id="a9107-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="a9107-107">Этот результат проходит через любые входные альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="a9107-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="a9107-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1HueToRgb.</span><span class="sxs-lookup"><span data-stu-id="a9107-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="a9107-109">Чтобы изменить поведение этого действия, используйте [эффекты оттенка RGB](rgb-to-hue-effect.md).</span><span class="sxs-lookup"><span data-stu-id="a9107-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="a9107-110">Образец кода</span><span class="sxs-lookup"><span data-stu-id="a9107-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="a9107-111">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="a9107-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a9107-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a9107-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a9107-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a9107-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="a9107-114">Пример кода</span><span class="sxs-lookup"><span data-stu-id="a9107-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="a9107-115">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="a9107-115">Effect properties</span></span>

<span data-ttu-id="a9107-116">Свойства для эффектов контрастности определяются перечислением [**D2D1 \_ хуеторгб \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .</span><span class="sxs-lookup"><span data-stu-id="a9107-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9107-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a9107-117">Requirements</span></span>



| <span data-ttu-id="a9107-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a9107-118">Requirement</span></span> | <span data-ttu-id="a9107-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a9107-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="a9107-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9107-120">Minimum supported client</span></span> | <span data-ttu-id="a9107-121">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="a9107-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a9107-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9107-122">Minimum supported server</span></span> | <span data-ttu-id="a9107-123">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="a9107-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a9107-124">Header</span><span class="sxs-lookup"><span data-stu-id="a9107-124">Header</span></span>                   | <span data-ttu-id="a9107-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="a9107-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="a9107-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a9107-126">Library</span></span>                  | <span data-ttu-id="a9107-127">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="a9107-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="a9107-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a9107-128">Related topics</span></span>

* [<span data-ttu-id="a9107-129">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="a9107-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
