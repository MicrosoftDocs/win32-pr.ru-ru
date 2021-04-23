---
title: Вигнетте, результат
description: Постепенно уменьшает входной рисунок на краях до заданного пользователем цвета.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136735"
---
# <a name="vignette-effect"></a><span data-ttu-id="5f8a9-103">Вигнетте, результат</span><span class="sxs-lookup"><span data-stu-id="5f8a9-103">Vignette effect</span></span>

<span data-ttu-id="5f8a9-104">Постепенно уменьшает входной рисунок на краях до заданного пользователем цвета.</span><span class="sxs-lookup"><span data-stu-id="5f8a9-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="5f8a9-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Vignette.</span><span class="sxs-lookup"><span data-stu-id="5f8a9-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="5f8a9-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="5f8a9-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="5f8a9-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="5f8a9-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="5f8a9-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="5f8a9-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5f8a9-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5f8a9-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5f8a9-110">См. также</span><span class="sxs-lookup"><span data-stu-id="5f8a9-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5f8a9-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="5f8a9-111">Example image</span></span>

![Пример выходных данных эффектов](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="5f8a9-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="5f8a9-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="5f8a9-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="5f8a9-114">Effect properties</span></span>

<span data-ttu-id="5f8a9-115">Свойства для вигнеттеного действия определяются перечислением [**D2D1 \_ вигнетте \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) .</span><span class="sxs-lookup"><span data-stu-id="5f8a9-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8a9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5f8a9-116">Requirements</span></span>

| <span data-ttu-id="5f8a9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5f8a9-117">Requirement</span></span> | <span data-ttu-id="5f8a9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5f8a9-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="5f8a9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5f8a9-119">Minimum supported client</span></span> | <span data-ttu-id="5f8a9-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="5f8a9-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5f8a9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5f8a9-121">Minimum supported server</span></span> | <span data-ttu-id="5f8a9-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="5f8a9-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5f8a9-123">Header</span><span class="sxs-lookup"><span data-stu-id="5f8a9-123">Header</span></span>                   | <span data-ttu-id="5f8a9-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="5f8a9-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="5f8a9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5f8a9-125">Library</span></span>                  | <span data-ttu-id="5f8a9-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="5f8a9-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="5f8a9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="5f8a9-127">Related topics</span></span>

* [<span data-ttu-id="5f8a9-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="5f8a9-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
