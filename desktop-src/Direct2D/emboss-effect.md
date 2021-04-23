---
title: Эффект приподнятости
description: Создает версию изображения в градациях серого, которая отображается, как будто она помечена на бумаге.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802302"
---
# <a name="emboss-effect"></a><span data-ttu-id="a919d-103">Эффект приподнятости</span><span class="sxs-lookup"><span data-stu-id="a919d-103">Emboss effect</span></span>

<span data-ttu-id="a919d-104">Создает версию изображения в градациях серого, которая отображается, как будто она помечена на бумаге.</span><span class="sxs-lookup"><span data-stu-id="a919d-104">Creates a grayscale version of the image that appears as though it has been stamped into paper.</span></span>

<span data-ttu-id="a919d-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Emboss.</span><span class="sxs-lookup"><span data-stu-id="a919d-105">The CLSID for this effect is CLSID\_D2D1Emboss.</span></span>

-   [<span data-ttu-id="a919d-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="a919d-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="a919d-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="a919d-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="a919d-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="a919d-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a919d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="a919d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a919d-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a919d-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="a919d-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="a919d-111">Example image</span></span>

![Пример выходных данных эффектов](images/emboss-effect.png)

## <a name="sample-code"></a><span data-ttu-id="a919d-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="a919d-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="a919d-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="a919d-114">Effect properties</span></span>

<span data-ttu-id="a919d-115">Свойства эффекта приподнятия определяются перечислением [**D2D1 \_ тиснение \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) .</span><span class="sxs-lookup"><span data-stu-id="a919d-115">The properties for the emboss effect are defined by the [**D2D1\_EMBOSS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a919d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a919d-116">Requirements</span></span>



| <span data-ttu-id="a919d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a919d-117">Requirement</span></span> | <span data-ttu-id="a919d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a919d-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="a919d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a919d-119">Minimum supported client</span></span> | <span data-ttu-id="a919d-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="a919d-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a919d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a919d-121">Minimum supported server</span></span> | <span data-ttu-id="a919d-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="a919d-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a919d-123">Header</span><span class="sxs-lookup"><span data-stu-id="a919d-123">Header</span></span>                   | <span data-ttu-id="a919d-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="a919d-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="a919d-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a919d-125">Library</span></span>                  | <span data-ttu-id="a919d-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="a919d-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="a919d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a919d-127">Related topics</span></span>

* [<span data-ttu-id="a919d-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="a919d-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
