---
description: Асинхронный запрос для получения сводных сведений о журнале графики.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исуммарирекуест:: Рекуестасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710650"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="fe54a-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>Метод Исуммарирекуест:: Рекуестасинк</span><span class="sxs-lookup"><span data-stu-id="fe54a-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="fe54a-104">Асинхронный запрос для получения сводных сведений о журнале графики.</span><span class="sxs-lookup"><span data-stu-id="fe54a-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe54a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe54a-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fe54a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe54a-106">Parameters</span></span>

<span data-ttu-id="fe54a-107">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="fe54a-107">*requestCallback* </span></span>  
<span data-ttu-id="fe54a-108">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="fe54a-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fe54a-109">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="fe54a-109">*requestCookie* </span></span>  
<span data-ttu-id="fe54a-110">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="fe54a-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fe54a-111">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="fe54a-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fe54a-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="fe54a-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe54a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe54a-113">Return value</span></span>

<span data-ttu-id="fe54a-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fe54a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe54a-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fe54a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe54a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fe54a-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe54a-117">Header</span><span class="sxs-lookup"><span data-stu-id="fe54a-117">Header</span></span></p></td><td><span data-ttu-id="fe54a-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="fe54a-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fe54a-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="fe54a-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fe54a-120">**исуммарирекуест**</span><span class="sxs-lookup"><span data-stu-id="fe54a-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
