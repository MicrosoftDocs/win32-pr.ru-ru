---
title: Эффект выделения и теней
description: Регулирует выделение и тени изображения.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104568642"
---
# <a name="highlights-and-shadows-effect"></a><span data-ttu-id="37924-103">Эффект выделения и теней</span><span class="sxs-lookup"><span data-stu-id="37924-103">Highlights and shadows effect</span></span>

<span data-ttu-id="37924-104">Регулирует выделение и тени изображения.</span><span class="sxs-lookup"><span data-stu-id="37924-104">Adjusts the highlights and shadows of the image.</span></span>

<span data-ttu-id="37924-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1HighlightsShadows.</span><span class="sxs-lookup"><span data-stu-id="37924-105">The CLSID for this effect is CLSID\_D2D1HighlightsShadows.</span></span>

-   [<span data-ttu-id="37924-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="37924-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="37924-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="37924-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="37924-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="37924-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="37924-109">Требования</span><span class="sxs-lookup"><span data-stu-id="37924-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="37924-110">См. также</span><span class="sxs-lookup"><span data-stu-id="37924-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="37924-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="37924-111">Example image</span></span>

![Пример выходных данных эффектов](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a><span data-ttu-id="37924-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="37924-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="37924-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="37924-114">Effect properties</span></span>

<span data-ttu-id="37924-115">Свойства для эффектов светлых и темных значений определяются перечислением [**D2D1 \_ хигхлигхтсандшадовс \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) .</span><span class="sxs-lookup"><span data-stu-id="37924-115">The properties for the highlights and shadows effect are defined by the [**D2D1\_HIGHLIGHTSANDSHADOWS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="37924-116">Требования</span><span class="sxs-lookup"><span data-stu-id="37924-116">Requirements</span></span>

| <span data-ttu-id="37924-117">Требование</span><span class="sxs-lookup"><span data-stu-id="37924-117">Requirement</span></span> | <span data-ttu-id="37924-118">Значение</span><span class="sxs-lookup"><span data-stu-id="37924-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="37924-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37924-119">Minimum supported client</span></span> | <span data-ttu-id="37924-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="37924-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="37924-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37924-121">Minimum supported server</span></span> | <span data-ttu-id="37924-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="37924-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="37924-123">Header</span><span class="sxs-lookup"><span data-stu-id="37924-123">Header</span></span>                   | <span data-ttu-id="37924-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="37924-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="37924-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37924-125">Library</span></span>                  | <span data-ttu-id="37924-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="37924-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="37924-127">См. также</span><span class="sxs-lookup"><span data-stu-id="37924-127">Related topics</span></span>

* [<span data-ttu-id="37924-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="37924-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
