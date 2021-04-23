---
description: Запрашивает список событий, которые вызывают изменение в указанном пикселе, прорисовку целевого объекта/UAV и кадра.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixelHistoryRequest2:: Рекуестинтерсектионс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537319"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="5b07d-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>Метод IPixelHistoryRequest2:: Рекуестинтерсектионс</span><span class="sxs-lookup"><span data-stu-id="5b07d-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="5b07d-104">Запрашивает список событий, которые вызывают изменение в указанном пикселе, прорисовку целевого объекта/UAV и кадра.</span><span class="sxs-lookup"><span data-stu-id="5b07d-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b07d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b07d-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="5b07d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b07d-106">Parameters</span></span>

<span data-ttu-id="5b07d-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="5b07d-107">*frameNumber* </span></span>  
<span data-ttu-id="5b07d-108">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="5b07d-108">The specified frame.</span></span>

<span data-ttu-id="5b07d-109">*растров* </span><span class="sxs-lookup"><span data-stu-id="5b07d-109">*pixel* </span></span>  
<span data-ttu-id="5b07d-110">Указанный пиксель.</span><span class="sxs-lookup"><span data-stu-id="5b07d-110">The specified pixel.</span></span>

<span data-ttu-id="5b07d-111">*рендертаржетптр* </span><span class="sxs-lookup"><span data-stu-id="5b07d-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="5b07d-112">Адрес указанного целевого объекта прорисовки</span><span class="sxs-lookup"><span data-stu-id="5b07d-112">The address of the specified render target</span></span>

<span data-ttu-id="5b07d-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="5b07d-113">*requestCallback* </span></span>  
<span data-ttu-id="5b07d-114">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="5b07d-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="5b07d-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="5b07d-115">*requestCookie* </span></span>  
<span data-ttu-id="5b07d-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="5b07d-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="5b07d-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="5b07d-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="5b07d-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5b07d-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b07d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b07d-119">Return value</span></span>

<span data-ttu-id="5b07d-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b07d-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b07d-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b07d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b07d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5b07d-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5b07d-123">Header</span><span class="sxs-lookup"><span data-stu-id="5b07d-123">Header</span></span></p></td><td><span data-ttu-id="5b07d-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="5b07d-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5b07d-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="5b07d-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5b07d-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="5b07d-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
