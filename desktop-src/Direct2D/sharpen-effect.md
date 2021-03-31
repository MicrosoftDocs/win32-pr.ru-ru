---
title: Эффекты резкости
description: Повышает резкость изображения.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802033"
---
# <a name="sharpen-effect"></a><span data-ttu-id="18752-103">Эффекты резкости</span><span class="sxs-lookup"><span data-stu-id="18752-103">Sharpen effect</span></span>

<span data-ttu-id="18752-104">Повышает резкость изображения.</span><span class="sxs-lookup"><span data-stu-id="18752-104">Sharpens the image.</span></span>

<span data-ttu-id="18752-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Sharpen.</span><span class="sxs-lookup"><span data-stu-id="18752-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="18752-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="18752-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="18752-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="18752-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="18752-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="18752-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="18752-109">Требования</span><span class="sxs-lookup"><span data-stu-id="18752-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="18752-110">См. также</span><span class="sxs-lookup"><span data-stu-id="18752-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="18752-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="18752-111">Example image</span></span>

![Пример выходных данных эффектов](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="18752-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="18752-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="18752-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="18752-114">Effect properties</span></span>

<span data-ttu-id="18752-115">Свойства для эффектов резкости определяются перечислением [**D2D1 \_ резкость \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .</span><span class="sxs-lookup"><span data-stu-id="18752-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="18752-116">Требования</span><span class="sxs-lookup"><span data-stu-id="18752-116">Requirements</span></span>



| <span data-ttu-id="18752-117">Требование</span><span class="sxs-lookup"><span data-stu-id="18752-117">Requirement</span></span> | <span data-ttu-id="18752-118">Значение</span><span class="sxs-lookup"><span data-stu-id="18752-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="18752-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18752-119">Minimum supported client</span></span> | <span data-ttu-id="18752-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="18752-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="18752-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18752-121">Minimum supported server</span></span> | <span data-ttu-id="18752-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="18752-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="18752-123">Header</span><span class="sxs-lookup"><span data-stu-id="18752-123">Header</span></span>                   | <span data-ttu-id="18752-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="18752-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="18752-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18752-125">Library</span></span>                  | <span data-ttu-id="18752-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="18752-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="18752-127">См. также</span><span class="sxs-lookup"><span data-stu-id="18752-127">Related topics</span></span>

* [<span data-ttu-id="18752-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="18752-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



