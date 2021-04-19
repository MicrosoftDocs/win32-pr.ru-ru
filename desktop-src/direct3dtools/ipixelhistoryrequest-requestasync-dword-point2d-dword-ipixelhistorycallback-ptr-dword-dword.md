---
description: Запрашивает список результатов журнала пикселей в указанном пикселе, визуализирует целевой/УАВ и Frame.
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипикселхисторирекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538198"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="fbc86-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>Метод Ипикселхисторирекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="fbc86-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="fbc86-104">Запрашивает список результатов журнала пикселей в указанном пикселе, визуализирует целевой/УАВ и Frame.</span><span class="sxs-lookup"><span data-stu-id="fbc86-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc86-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbc86-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fbc86-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbc86-106">Parameters</span></span>

<span data-ttu-id="fbc86-107">*фраменумбер* </span><span class="sxs-lookup"><span data-stu-id="fbc86-107">*frameNumber* </span></span>  
<span data-ttu-id="fbc86-108">Указанный кадр.</span><span class="sxs-lookup"><span data-stu-id="fbc86-108">The specified frame.</span></span>

<span data-ttu-id="fbc86-109">*растров* </span><span class="sxs-lookup"><span data-stu-id="fbc86-109">*pixel* </span></span>  
<span data-ttu-id="fbc86-110">Указанный пиксель.</span><span class="sxs-lookup"><span data-stu-id="fbc86-110">The specified pixel.</span></span>

<span data-ttu-id="fbc86-111">*рендертаржетптр* </span><span class="sxs-lookup"><span data-stu-id="fbc86-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="fbc86-112">Указанный целевой объект прорисовки.</span><span class="sxs-lookup"><span data-stu-id="fbc86-112">The specified render target.</span></span>

<span data-ttu-id="fbc86-113">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="fbc86-113">*requestCallback* </span></span>  
<span data-ttu-id="fbc86-114">Адрес обратного вызова, используемый для нотифифи узла результатов.</span><span class="sxs-lookup"><span data-stu-id="fbc86-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="fbc86-115">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="fbc86-115">*requestCookie* </span></span>  
<span data-ttu-id="fbc86-116">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="fbc86-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fbc86-117">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="fbc86-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fbc86-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fbc86-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbc86-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbc86-119">Return value</span></span>

<span data-ttu-id="fbc86-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fbc86-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbc86-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbc86-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc86-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fbc86-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fbc86-123">Header</span><span class="sxs-lookup"><span data-stu-id="fbc86-123">Header</span></span></p></td><td><span data-ttu-id="fbc86-124">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="fbc86-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fbc86-125"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="fbc86-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fbc86-126">**ипикселхисторирекуест**</span><span class="sxs-lookup"><span data-stu-id="fbc86-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
