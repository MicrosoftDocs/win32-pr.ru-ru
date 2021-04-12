---
description: Функция обратного вызова, используемая для уведомления узла о ходе автономного анализа.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisProgress\_DWORD\_DOUBLE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисискаллбакк:: Оффлинеаналисиспрогресс'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 17847FD7-A10A-4E52-90AD-ADE446D87E73
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisProgress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4184be5d8d40b0ef46fe5e0029e9e4b1f38cf120
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423129"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span data-ttu-id="2b98c-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>Метод Иоффлинеаналисискаллбакк:: Оффлинеаналисиспрогресс</span><span class="sxs-lookup"><span data-stu-id="2b98c-103"><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>IOfflineAnalysisCallback::OfflineAnalysisProgress method</span></span>

<span data-ttu-id="2b98c-104">Функция обратного вызова, используемая для уведомления узла о ходе автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="2b98c-104">A callback function used to notify the host of offline analysis progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b98c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b98c-105">Syntax</span></span>


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a><span data-ttu-id="2b98c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b98c-106">Parameters</span></span>

<span data-ttu-id="2b98c-107">*"* </span><span class="sxs-lookup"><span data-stu-id="2b98c-107">*cookie* </span></span>  
<span data-ttu-id="2b98c-108">Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.</span><span class="sxs-lookup"><span data-stu-id="2b98c-108">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="2b98c-109">*двигается* </span><span class="sxs-lookup"><span data-stu-id="2b98c-109">*progress* </span></span>  
<span data-ttu-id="2b98c-110">Процент выполнения.</span><span class="sxs-lookup"><span data-stu-id="2b98c-110">The progress percentage.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b98c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b98c-111">Return value</span></span>

<span data-ttu-id="2b98c-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2b98c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b98c-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b98c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b98c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2b98c-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2b98c-115">Header</span><span class="sxs-lookup"><span data-stu-id="2b98c-115">Header</span></span></p></td><td><span data-ttu-id="2b98c-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="2b98c-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="2b98c-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="2b98c-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="2b98c-118">**иоффлинеаналисискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="2b98c-118">**IOfflineAnalysisCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
