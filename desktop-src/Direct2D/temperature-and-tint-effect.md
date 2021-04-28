---
title: Воздействие на температуру и оттенок
description: Воздействие на температуру и оттенок
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096642"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="fc00b-103">Воздействие на температуру и оттенок</span><span class="sxs-lookup"><span data-stu-id="fc00b-103">Temperature and tint effect</span></span>

<span data-ttu-id="fc00b-104">Идентификатором CLSID для этого действия является CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="fc00b-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="fc00b-105">Образец кода</span><span class="sxs-lookup"><span data-stu-id="fc00b-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="fc00b-106">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="fc00b-106">Effect properties</span></span>

<span data-ttu-id="fc00b-107">Свойства для эффектов температуры и оттенка определяются перечислением [**D2D1 \_ температуреандтинт \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) .</span><span class="sxs-lookup"><span data-stu-id="fc00b-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc00b-108">Требования</span><span class="sxs-lookup"><span data-stu-id="fc00b-108">Requirements</span></span>



| <span data-ttu-id="fc00b-109">Требование</span><span class="sxs-lookup"><span data-stu-id="fc00b-109">Requirement</span></span> | <span data-ttu-id="fc00b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fc00b-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="fc00b-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc00b-111">Minimum supported client</span></span> | <span data-ttu-id="fc00b-112">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="fc00b-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fc00b-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc00b-113">Minimum supported server</span></span> | <span data-ttu-id="fc00b-114">Приложения для \[ магазина Windows для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="fc00b-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fc00b-115">Header</span><span class="sxs-lookup"><span data-stu-id="fc00b-115">Header</span></span>                   | <span data-ttu-id="fc00b-116">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="fc00b-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="fc00b-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc00b-117">Library</span></span>                  | <span data-ttu-id="fc00b-118">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="fc00b-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="fc00b-119">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="fc00b-119">Related topics</span></span>

* [<span data-ttu-id="fc00b-120">Интерфейс ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="fc00b-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
