---
title: Воздействие на выдержки
description: Увеличение или уменьшение экспозиции изображения.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989040"
---
# <a name="exposure-effect"></a><span data-ttu-id="bf7ba-103">Воздействие на выдержки</span><span class="sxs-lookup"><span data-stu-id="bf7ba-103">Exposure effect</span></span>

<span data-ttu-id="bf7ba-104">Увеличение или уменьшение экспозиции изображения.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="bf7ba-105">Идентификатором CLSID для этого действия является CLSID \_ D2D1Exposure.</span><span class="sxs-lookup"><span data-stu-id="bf7ba-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="bf7ba-106">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="bf7ba-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="bf7ba-107">Образец кода</span><span class="sxs-lookup"><span data-stu-id="bf7ba-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="bf7ba-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="bf7ba-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="bf7ba-109">Требования</span><span class="sxs-lookup"><span data-stu-id="bf7ba-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bf7ba-110">См. также</span><span class="sxs-lookup"><span data-stu-id="bf7ba-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="bf7ba-111">Пример изображения</span><span class="sxs-lookup"><span data-stu-id="bf7ba-111">Example image</span></span>

![Пример выходных данных эффектов](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="bf7ba-113">Пример кода</span><span class="sxs-lookup"><span data-stu-id="bf7ba-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="bf7ba-114">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="bf7ba-114">Effect properties</span></span>

<span data-ttu-id="bf7ba-115">Свойства для влияния на выдержки определяются перечислением [**D2D1 \_ экспозиции \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .</span><span class="sxs-lookup"><span data-stu-id="bf7ba-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7ba-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bf7ba-116">Requirements</span></span>



| <span data-ttu-id="bf7ba-117">Требование</span><span class="sxs-lookup"><span data-stu-id="bf7ba-117">Requirement</span></span> | <span data-ttu-id="bf7ba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bf7ba-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="bf7ba-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf7ba-119">Minimum supported client</span></span> | <span data-ttu-id="bf7ba-120">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf7ba-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bf7ba-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf7ba-121">Minimum supported server</span></span> | <span data-ttu-id="bf7ba-122">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf7ba-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bf7ba-123">Header</span><span class="sxs-lookup"><span data-stu-id="bf7ba-123">Header</span></span>                   | <span data-ttu-id="bf7ba-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="bf7ba-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="bf7ba-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf7ba-125">Library</span></span>                  | <span data-ttu-id="bf7ba-126">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="bf7ba-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="bf7ba-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bf7ba-127">Related topics</span></span>

* [<span data-ttu-id="bf7ba-128">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="bf7ba-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




