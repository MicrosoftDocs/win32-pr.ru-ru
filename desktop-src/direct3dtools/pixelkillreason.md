---
description: Перечисление, используемое для указания причины отклонения пикселя.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление ПИКСЕЛКИЛЛРЕАСОН
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341822"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span data-ttu-id="f8df5-103"><span id="vspixengine.pixelkillreason"></span>Перечисление ПИКСЕЛКИЛЛРЕАСОН</span><span class="sxs-lookup"><span data-stu-id="f8df5-103"><span id="vspixengine.pixelkillreason"></span>PIXELKILLREASON enumeration</span></span>

<span data-ttu-id="f8df5-104">Перечисление, используемое для указания причины отклонения пикселя.</span><span class="sxs-lookup"><span data-stu-id="f8df5-104">An enum used to indicate why a pixel was rejected.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8df5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8df5-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="f8df5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f8df5-106">Constants</span></span>

<span data-ttu-id="f8df5-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**ПКР \_ None**</span><span class="sxs-lookup"><span data-stu-id="f8df5-107"><span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR\_NONE**</span></span>  
<span data-ttu-id="f8df5-108">Значение, указывающее, что пиксель не был отклонен.</span><span class="sxs-lookup"><span data-stu-id="f8df5-108">A value that indicates that the pixel was not rejected.</span></span>

<span data-ttu-id="f8df5-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**ПКР \_ шадеркилл**</span><span class="sxs-lookup"><span data-stu-id="f8df5-109"><span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR\_SHADERKILL**</span></span>  
<span data-ttu-id="f8df5-110">Значение, указывающее, что точка была отклонена из-за того, что шейдер не выполнялся.</span><span class="sxs-lookup"><span data-stu-id="f8df5-110">A value that indicates that the pixel was rejected because the shader didn't run.</span></span>

<span data-ttu-id="f8df5-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**ПКР \_ сЦиссортест**</span><span class="sxs-lookup"><span data-stu-id="f8df5-111"><span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR\_SCISSORTEST**</span></span>  
<span data-ttu-id="f8df5-112">Значение, указывающее, что точка была отклонена из-за сбоя выножницного теста.</span><span class="sxs-lookup"><span data-stu-id="f8df5-112">A value that indicates that the pixel was rejected because the scissor test failed.</span></span>

<span data-ttu-id="f8df5-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**ПКР \_ алфатест**</span><span class="sxs-lookup"><span data-stu-id="f8df5-113"><span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR\_ALPHATEST**</span></span>  
<span data-ttu-id="f8df5-114">Значение, указывающее, что точка была отклонена из-за сбоя при проверке альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="f8df5-114">A value that indicates that the pixel was rejected because the alpha test failed.</span></span>

<span data-ttu-id="f8df5-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**ПКР \_ стенЦилтест**</span><span class="sxs-lookup"><span data-stu-id="f8df5-115"><span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR\_STENCILTEST**</span></span>  
<span data-ttu-id="f8df5-116">Значение, указывающее, что точка была отклонена из-за сбоя теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="f8df5-116">A value that indicates that the pixel was rejected because the stencil test failed.</span></span>

<span data-ttu-id="f8df5-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**ПКР \_ депстест**</span><span class="sxs-lookup"><span data-stu-id="f8df5-117"><span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR\_DEPTHTEST**</span></span>  
<span data-ttu-id="f8df5-118">Значение, указывающее, что точка была отклонена из-за сбоя теста глубины.</span><span class="sxs-lookup"><span data-stu-id="f8df5-118">A value that indicates that the pixel was rejected because the depth test failed.</span></span>

<span data-ttu-id="f8df5-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**ПКР \_ ноткомпутабле**</span><span class="sxs-lookup"><span data-stu-id="f8df5-119"><span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR\_NOTCOMPUTABLE**</span></span>  
<span data-ttu-id="f8df5-120">Значение, указывающее, что невозможно вычислить Журнал пикселей.</span><span class="sxs-lookup"><span data-stu-id="f8df5-120">A value that indicates that the pixel history can't be computed.</span></span>

<span data-ttu-id="f8df5-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**ПКР, \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="f8df5-121"><span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR\_ERROR**</span></span>  
<span data-ttu-id="f8df5-122">Значение, указывающее, что точка была отклонена из-за общей ошибки.</span><span class="sxs-lookup"><span data-stu-id="f8df5-122">A value that indicates that the pixel was rejected because of a general error.</span></span>

<span data-ttu-id="f8df5-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**ПКР, не \_ ПЕРЕсечение**</span><span class="sxs-lookup"><span data-stu-id="f8df5-123"><span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR\_NOINTERSECTION**</span></span>  
<span data-ttu-id="f8df5-124">Значение, указывающее, что точка была отклонена, поскольку вызов Draw не пересекает пиксел.</span><span class="sxs-lookup"><span data-stu-id="f8df5-124">A value that indicates that the pixel was rejected because the draw call does not intersect the pixel.</span></span>

<span data-ttu-id="f8df5-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**ПКР \_ перекрыто**</span><span class="sxs-lookup"><span data-stu-id="f8df5-125"><span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR\_OCCLUDED**</span></span>  
<span data-ttu-id="f8df5-126">Значение, указывающее, что точка была отклонена, поскольку Draw была перекрыто.</span><span class="sxs-lookup"><span data-stu-id="f8df5-126">A value that indicates that the pixel was rejected because the draw was occluded.</span></span>

<span data-ttu-id="f8df5-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**ПКР \_ депсстенЦилтест**</span><span class="sxs-lookup"><span data-stu-id="f8df5-127"><span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR\_DEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="f8df5-128">Значение, указывающее, что точка была отклонена из-за сбоя теста глубины и трафарета.</span><span class="sxs-lookup"><span data-stu-id="f8df5-128">A value that indicates that the pixel was rejected because the depth and stencil test failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8df5-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f8df5-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f8df5-130">Header</span><span class="sxs-lookup"><span data-stu-id="f8df5-130">Header</span></span></p></td><td><span data-ttu-id="f8df5-131">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f8df5-131">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



