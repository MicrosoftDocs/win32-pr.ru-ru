---
title: Воздействие на обнаружение границ
description: Отфильтровывает содержимое изображения, открывая линии на краях контрастных разделов изображения.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072025"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="1fa15-103">Воздействие на обнаружение границ</span><span class="sxs-lookup"><span data-stu-id="1fa15-103">Edge-detection effect</span></span>

<span data-ttu-id="1fa15-104">Отфильтровывает содержимое изображения, открывая линии на краях контрастных разделов изображения.</span><span class="sxs-lookup"><span data-stu-id="1fa15-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="1fa15-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1EdgeDetection.</span><span class="sxs-lookup"><span data-stu-id="1fa15-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="1fa15-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="1fa15-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="1fa15-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="1fa15-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="1fa15-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="1fa15-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="1fa15-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1fa15-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1fa15-110">См. также</span><span class="sxs-lookup"><span data-stu-id="1fa15-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="1fa15-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="1fa15-111">Example image</span></span>

![Пример выходных данных эффектов](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="1fa15-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="1fa15-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="1fa15-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="1fa15-114">Effect properties</span></span>

<span data-ttu-id="1fa15-115">Свойства для воздействия на обнаружение границ определяются перечислением [**D2D1 \_ еджедетектион \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) .</span><span class="sxs-lookup"><span data-stu-id="1fa15-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa15-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1fa15-116">Requirements</span></span>



| <span data-ttu-id="1fa15-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1fa15-117">Requirement</span></span> | <span data-ttu-id="1fa15-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1fa15-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="1fa15-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fa15-119">Minimum supported client</span></span> | <span data-ttu-id="1fa15-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="1fa15-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1fa15-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fa15-121">Minimum supported server</span></span> | <span data-ttu-id="1fa15-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="1fa15-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1fa15-123">Header</span><span class="sxs-lookup"><span data-stu-id="1fa15-123">Header</span></span>                   | <span data-ttu-id="1fa15-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="1fa15-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="1fa15-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1fa15-125">Library</span></span>                  | <span data-ttu-id="1fa15-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="1fa15-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="1fa15-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1fa15-127">Related topics</span></span>

* [<span data-ttu-id="1fa15-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="1fa15-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
