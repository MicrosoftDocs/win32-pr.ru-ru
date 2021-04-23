---
description: Запросы на отмену автономного анализа в запросе автономного анализа.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_CancelOfflineAnalysisAsync\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисисрекуест:: Канцелоффлинеаналисисасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 20107890-DF7B-4483-9D2C-1D9164366504
api_name:
- IOfflineAnalysisRequest.CancelOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79329d27aff74efb7d08c7cc182ddb6e21f96cba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494877"
---
# <a name="span-idvspixengineiofflineanalysisrequest_cancelofflineanalysisasync_dwordspaniofflineanalysisrequestcancelofflineanalysisasync-method"></a><span data-ttu-id="efac5-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>Метод Иоффлинеаналисисрекуест:: Канцелоффлинеаналисисасинк</span><span class="sxs-lookup"><span data-stu-id="efac5-103"><span id="vspixengine.iofflineanalysisrequest_cancelofflineanalysisasync_dword"></span>IOfflineAnalysisRequest::CancelOfflineAnalysisAsync method</span></span>

<span data-ttu-id="efac5-104">Запросы на отмену автономного анализа в запросе автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="efac5-104">Requests to cancel offline analysis in an offline analysis request.</span></span>

## <a name="syntax"></a><span data-ttu-id="efac5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efac5-105">Syntax</span></span>


```C++
HRESULT CancelOfflineAnalysisAsync(
   DWORD cookie
);
```

## <a name="parameters"></a><span data-ttu-id="efac5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efac5-106">Parameters</span></span>

<span data-ttu-id="efac5-107">*"* </span><span class="sxs-lookup"><span data-stu-id="efac5-107">*cookie* </span></span>  
<span data-ttu-id="efac5-108">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="efac5-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

## <a name="return-value"></a><span data-ttu-id="efac5-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efac5-109">Return value</span></span>

<span data-ttu-id="efac5-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="efac5-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="efac5-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="efac5-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="efac5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="efac5-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="efac5-113">Header</span><span class="sxs-lookup"><span data-stu-id="efac5-113">Header</span></span></p></td><td><span data-ttu-id="efac5-114">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="efac5-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="efac5-115"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="efac5-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="efac5-116">**иоффлинеаналисисрекуест**</span><span class="sxs-lookup"><span data-stu-id="efac5-116">**IOfflineAnalysisRequest**</span></span>](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
