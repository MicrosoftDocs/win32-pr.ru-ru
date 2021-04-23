---
description: Обратный вызов, уведомляющий узел о размещении сведений о пересечении журнала пикселей, возвращаемых запросом связана.
MS-HAID: vspixengine.IPixelHistoryCallback2\_IntersectionsCallback\_DWORD\_PixelHistoryIntersection\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixelHistoryCallback2:: Интерсектионскаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 478B2495-93E4-4BB1-BC86-802D2AFAF97D
api_name:
- IPixelHistoryCallback2.IntersectionsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 30bde17a2c504b2afdaf9c13a7b6d7014590b1dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139882"
---
# <a name="span-idvspixengineipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arrspanipixelhistorycallback2intersectionscallback-method"></a><span data-ttu-id="c6572-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>Метод IPixelHistoryCallback2:: Интерсектионскаллбакк</span><span class="sxs-lookup"><span data-stu-id="c6572-103"><span id="vspixengine.ipixelhistorycallback2_intersectionscallback_dword_pixelhistoryintersection_arr"></span>IPixelHistoryCallback2::IntersectionsCallback method</span></span>

<span data-ttu-id="c6572-104">Обратный вызов, уведомляющий узел о размещении сведений о пересечении журнала пикселей, возвращаемых запросом связана.</span><span class="sxs-lookup"><span data-stu-id="c6572-104">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6572-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6572-105">Syntax</span></span>


```C++
HRESULT IntersectionsCallback(
   DWORD                       count,
   PixelHistoryIntersection [] count0_intersections
);
```

## <a name="parameters"></a><span data-ttu-id="c6572-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6572-106">Parameters</span></span>

<span data-ttu-id="c6572-107">*расчета* </span><span class="sxs-lookup"><span data-stu-id="c6572-107">*count* </span></span>  
<span data-ttu-id="c6572-108">Число пересечения в журнале пикселей.</span><span class="sxs-lookup"><span data-stu-id="c6572-108">The number of pixel history intersections.</span></span>

<span data-ttu-id="c6572-109">*\_пересечения count0* </span><span class="sxs-lookup"><span data-stu-id="c6572-109">*count0\_intersections* </span></span>  
<span data-ttu-id="c6572-110">Пересечения с журналом пикселей.</span><span class="sxs-lookup"><span data-stu-id="c6572-110">The pixel history intersections.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6572-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6572-111">Return value</span></span>

<span data-ttu-id="c6572-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6572-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6572-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6572-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6572-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c6572-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c6572-115">Header</span><span class="sxs-lookup"><span data-stu-id="c6572-115">Header</span></span></p></td><td><span data-ttu-id="c6572-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c6572-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c6572-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="c6572-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c6572-118">**IPixelHistoryCallback2**</span><span class="sxs-lookup"><span data-stu-id="c6572-118">**IPixelHistoryCallback2**</span></span>](/windows/desktop/direct3dtools/ipixelhistorycallback2)

 

 
