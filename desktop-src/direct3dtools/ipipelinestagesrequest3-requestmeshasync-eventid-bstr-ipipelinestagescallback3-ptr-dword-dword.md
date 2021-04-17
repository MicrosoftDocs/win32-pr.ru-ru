---
description: Асинхронный запрос на получение данных сетки из указанного события.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesRequest3:: Рекуестмешасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710591"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="e0735-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>Метод IPipeLineStagesRequest3:: Рекуестмешасинк</span><span class="sxs-lookup"><span data-stu-id="e0735-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="e0735-104">Асинхронный запрос на получение данных сетки из указанного события.</span><span class="sxs-lookup"><span data-stu-id="e0735-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0735-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0735-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e0735-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0735-106">Parameters</span></span>

<span data-ttu-id="e0735-107">*1008* </span><span class="sxs-lookup"><span data-stu-id="e0735-107">*eventID* </span></span>  
<span data-ttu-id="e0735-108">Указанное событие.</span><span class="sxs-lookup"><span data-stu-id="e0735-108">The specified event.</span></span>

<span data-ttu-id="e0735-109">*мешфиленаме* </span><span class="sxs-lookup"><span data-stu-id="e0735-109">*meshFilename* </span></span>  
<span data-ttu-id="e0735-110">Строка COM, содержащая путь к файлу, в который записываются данные сетки.</span><span class="sxs-lookup"><span data-stu-id="e0735-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="e0735-111">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="e0735-111">*requestCallback* </span></span>  
<span data-ttu-id="e0735-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="e0735-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="e0735-113">*рекуесткукие* </span><span class="sxs-lookup"><span data-stu-id="e0735-113">*requestCookie* </span></span>  
<span data-ttu-id="e0735-114">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="e0735-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e0735-115">*прогрессинтервалмсекс* </span><span class="sxs-lookup"><span data-stu-id="e0735-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e0735-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e0735-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0735-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0735-117">Return value</span></span>

<span data-ttu-id="e0735-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e0735-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0735-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0735-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0735-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e0735-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e0735-121">Header</span><span class="sxs-lookup"><span data-stu-id="e0735-121">Header</span></span></p></td><td><span data-ttu-id="e0735-122">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="e0735-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e0735-123"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="e0735-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e0735-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="e0735-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
