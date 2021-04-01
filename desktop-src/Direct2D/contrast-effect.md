---
title: Контрастный результат
description: Увеличивает или уменьшает контрастность изображения.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071732"
---
# <a name="contrast-effect"></a><span data-ttu-id="d56ab-103">Контрастный результат</span><span class="sxs-lookup"><span data-stu-id="d56ab-103">Contrast effect</span></span>

<span data-ttu-id="d56ab-104">Увеличивает или уменьшает контрастность изображения.</span><span class="sxs-lookup"><span data-stu-id="d56ab-104">Increases or decreases the contrast of an image.</span></span>

<span data-ttu-id="d56ab-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Contrast.</span><span class="sxs-lookup"><span data-stu-id="d56ab-105">The CLSID for this effect is CLSID\_D2D1Contrast.</span></span>

<span data-ttu-id="d56ab-106">Функция контрастности изменяет каждое значение цветового канала с помощью двух кусочно-ных полиномов, которые соответствуют наклону непрерывности в точке (0,5, 0,5).</span><span class="sxs-lookup"><span data-stu-id="d56ab-106">The contrast function modifies each color channel value using two, piecewise quadratic polynomials that meet with slope continuity at the point (0.5, 0.5).</span></span>

![кусочно-ие одноквадратных коэффициентов, которые соответствуют наклону непрерывности в точке (0,5, 0,5)](images/contrast-effect-slope.png)

-   [<span data-ttu-id="d56ab-108">Примеры изображений</span><span class="sxs-lookup"><span data-stu-id="d56ab-108">Example Images</span></span>](#example-images)
-   [<span data-ttu-id="d56ab-109">Образец кода</span><span class="sxs-lookup"><span data-stu-id="d56ab-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="d56ab-110">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="d56ab-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d56ab-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d56ab-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d56ab-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d56ab-112">Related topics</span></span>](#related-topics)

## <a name="example-images"></a><span data-ttu-id="d56ab-113">Примеры изображений</span><span class="sxs-lookup"><span data-stu-id="d56ab-113">Example images</span></span>

<span data-ttu-id="d56ab-114">В этом примере показаны выходные данные результата с максимальной контрастностью (контраст = 1,0).</span><span class="sxs-lookup"><span data-stu-id="d56ab-114">This example shows the output of the effect with maximum contrast applied (Contrast = 1.0).</span></span>

<span data-ttu-id="d56ab-115">До</span><span class="sxs-lookup"><span data-stu-id="d56ab-115">Before</span></span>

![изображение перед применением эффектов](images/contrast-effect-before.png)

<span data-ttu-id="d56ab-117">После</span><span class="sxs-lookup"><span data-stu-id="d56ab-117">After</span></span>

![изображение после применения эффектов](images/contrast-effect-after.png)

## <a name="sample-code"></a><span data-ttu-id="d56ab-119">Пример кода</span><span class="sxs-lookup"><span data-stu-id="d56ab-119">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="d56ab-120">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="d56ab-120">Effect properties</span></span>

<span data-ttu-id="d56ab-121">Свойства для эффектов контрастности определяются перечислением [**\_ \_ prop контрастности D2D1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .</span><span class="sxs-lookup"><span data-stu-id="d56ab-121">The properties for the contrast effect are defined by the [**D2D1\_CONTRAST\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d56ab-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d56ab-122">Requirements</span></span>

| <span data-ttu-id="d56ab-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d56ab-123">Requirement</span></span> | <span data-ttu-id="d56ab-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d56ab-124">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="d56ab-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d56ab-125">Minimum supported client</span></span> | <span data-ttu-id="d56ab-126">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="d56ab-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d56ab-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d56ab-127">Minimum supported server</span></span> | <span data-ttu-id="d56ab-128">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="d56ab-128">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d56ab-129">Header</span><span class="sxs-lookup"><span data-stu-id="d56ab-129">Header</span></span>                   | <span data-ttu-id="d56ab-130">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="d56ab-130">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="d56ab-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d56ab-131">Library</span></span>                  | <span data-ttu-id="d56ab-132">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="d56ab-132">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="d56ab-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d56ab-133">Related topics</span></span>

* [<span data-ttu-id="d56ab-134">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="d56ab-134">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
