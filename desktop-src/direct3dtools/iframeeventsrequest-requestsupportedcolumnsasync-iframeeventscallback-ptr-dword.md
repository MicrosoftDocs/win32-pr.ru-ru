---
description: Асинхронный запрос для получения сведений о том, какие столбцы (поля) Этот тип запроса событий фрейма поддерживает.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамивентсрекуест:: Рекуестсуппортедколумнсасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806197"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="fd7fa-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>Метод Ифрамивентсрекуест:: Рекуестсуппортедколумнсасинк</span><span class="sxs-lookup"><span data-stu-id="fd7fa-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="fd7fa-104">Асинхронный запрос для получения сведений о том, какие столбцы (поля) Этот тип запроса событий фрейма поддерживает.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-104">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd7fa-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fd7fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd7fa-106">Parameters</span></span>

<span data-ttu-id="fd7fa-107">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="fd7fa-107">*requestCallback* </span></span>  
<span data-ttu-id="fd7fa-108">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fd7fa-109">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="fd7fa-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fd7fa-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fd7fa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd7fa-111">Return value</span></span>

<span data-ttu-id="fd7fa-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fd7fa-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd7fa-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd7fa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7fa-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fd7fa-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fd7fa-115">Header</span><span class="sxs-lookup"><span data-stu-id="fd7fa-115">Header</span></span></p></td><td><span data-ttu-id="fd7fa-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="fd7fa-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fd7fa-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="fd7fa-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fd7fa-118">**ифрамивентсрекуест**</span><span class="sxs-lookup"><span data-stu-id="fd7fa-118">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
