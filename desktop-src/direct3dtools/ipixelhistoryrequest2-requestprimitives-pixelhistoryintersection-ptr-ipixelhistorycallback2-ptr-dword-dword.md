---
description: Запрашивает список примитивов из определенного пересечения. Дополнительные сведения см. в описании функции члена Рекуестинтерсектионс.
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixelHistoryRequest2:: Рекуестпримитивес'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710609"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="62f49-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>Метод IPixelHistoryRequest2:: Рекуестпримитивес</span><span class="sxs-lookup"><span data-stu-id="62f49-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="62f49-105">Запрашивает список примитивов из определенного пересечения.</span><span class="sxs-lookup"><span data-stu-id="62f49-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="62f49-106">Дополнительные сведения см. в описании функции члена Рекуестинтерсектионс.</span><span class="sxs-lookup"><span data-stu-id="62f49-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f49-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62f49-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="62f49-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="62f49-108">Parameters</span></span>

<span data-ttu-id="62f49-109">*крайне* </span><span class="sxs-lookup"><span data-stu-id="62f49-109">*intersection* </span></span>  
<span data-ttu-id="62f49-110">Адрес указанного пересечения.</span><span class="sxs-lookup"><span data-stu-id="62f49-110">The address of the specified intersection.</span></span>

<span data-ttu-id="62f49-111">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="62f49-111">*requestCallback* </span></span>  
<span data-ttu-id="62f49-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="62f49-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="62f49-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="62f49-113">*requestCookie* </span></span>  
<span data-ttu-id="62f49-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="62f49-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="62f49-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="62f49-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="62f49-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="62f49-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="62f49-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62f49-117">Return value</span></span>

<span data-ttu-id="62f49-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="62f49-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62f49-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62f49-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f49-120">Требования</span><span class="sxs-lookup"><span data-stu-id="62f49-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="62f49-121">Header</span><span class="sxs-lookup"><span data-stu-id="62f49-121">Header</span></span></p></td><td><span data-ttu-id="62f49-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="62f49-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="62f49-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="62f49-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="62f49-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="62f49-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
