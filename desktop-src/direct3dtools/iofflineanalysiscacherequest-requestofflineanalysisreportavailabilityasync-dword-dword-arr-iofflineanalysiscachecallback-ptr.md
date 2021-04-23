---
description: Запросы на кэширование автономного отчета об анализе указанных кадров.
MS-HAID: vspixengine.IOfflineAnalysisCacheRequest\_RequestOfflineAnalysisReportAvailabilityAsync\_DWORD\_DWORD\_arr\_IOfflineAnalysisCacheCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисискачерекуест:: Рекуестоффлинеаналисисрепортаваилабилитясинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10FA71F8-813D-4788-92C8-00B30A9AE5CC
api_name:
- IOfflineAnalysisCacheRequest.RequestOfflineAnalysisReportAvailabilityAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e2dfdb1e2a2cc113f9585a818550dd60aa73ae2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538210"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span data-ttu-id="69fca-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>Метод Иоффлинеаналисискачерекуест:: Рекуестоффлинеаналисисрепортаваилабилитясинк</span><span class="sxs-lookup"><span data-stu-id="69fca-103"><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>IOfflineAnalysisCacheRequest::RequestOfflineAnalysisReportAvailabilityAsync method</span></span>

<span data-ttu-id="69fca-104">Запросы на кэширование автономного отчета об анализе указанных кадров.</span><span class="sxs-lookup"><span data-stu-id="69fca-104">Requests to cache offline analysis report of the specified frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69fca-105">Syntax</span></span>


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a><span data-ttu-id="69fca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69fca-106">Parameters</span></span>

<span data-ttu-id="69fca-107">*нумфрамес* </span><span class="sxs-lookup"><span data-stu-id="69fca-107">*numFrames* </span></span>  
<span data-ttu-id="69fca-108">Число кадров, для которых формируются отчеты об анализе.</span><span class="sxs-lookup"><span data-stu-id="69fca-108">The number of frames to generate analysis reports for.</span></span>

<span data-ttu-id="69fca-109">*count0 \_ фраменумберс* </span><span class="sxs-lookup"><span data-stu-id="69fca-109">*count0\_frameNumbers* </span></span>  
<span data-ttu-id="69fca-110">Указанные кадры.</span><span class="sxs-lookup"><span data-stu-id="69fca-110">The specified frames.</span></span>

<span data-ttu-id="69fca-111">*рекуесткаллбакк* </span><span class="sxs-lookup"><span data-stu-id="69fca-111">*requestCallback* </span></span>  
<span data-ttu-id="69fca-112">Адрес обратного вызова, используемый для уведомления узла о результатах.</span><span class="sxs-lookup"><span data-stu-id="69fca-112">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="69fca-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69fca-113">Return value</span></span>

<span data-ttu-id="69fca-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="69fca-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69fca-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69fca-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="69fca-116">Требования</span><span class="sxs-lookup"><span data-stu-id="69fca-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="69fca-117">Header</span><span class="sxs-lookup"><span data-stu-id="69fca-117">Header</span></span></p></td><td><span data-ttu-id="69fca-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="69fca-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="69fca-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="69fca-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="69fca-120">**иоффлинеаналисискачерекуест**</span><span class="sxs-lookup"><span data-stu-id="69fca-120">**IOfflineAnalysisCacheRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
