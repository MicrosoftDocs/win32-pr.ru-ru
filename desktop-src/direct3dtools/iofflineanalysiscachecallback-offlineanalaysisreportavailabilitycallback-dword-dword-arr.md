---
description: Функция обратного вызова, используемая для уведомления узла о том, какие кадры имеют доступ к автономным отчетам анализа.
MS-HAID: vspixengine.IOfflineAnalysisCacheCallback\_OfflineAnalaysisReportAvailabilityCallback\_DWORD\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисискачекаллбакк:: Оффлинеаналайсисрепортаваилабилитикаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2061EB62-4CBD-4668-BFCD-6E43014BB406
api_name:
- IOfflineAnalysisCacheCallback.OfflineAnalaysisReportAvailabilityCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: adbffbeb79aaf648c3319cf572dcbc905e9fd307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691996"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span data-ttu-id="b1d7b-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>Метод Иоффлинеаналисискачекаллбакк:: Оффлинеаналайсисрепортаваилабилитикаллбакк</span><span class="sxs-lookup"><span data-stu-id="b1d7b-103"><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>IOfflineAnalysisCacheCallback::OfflineAnalaysisReportAvailabilityCallback method</span></span>

<span data-ttu-id="b1d7b-104">Функция обратного вызова, используемая для уведомления узла о том, какие кадры имеют доступ к автономным отчетам анализа.</span><span class="sxs-lookup"><span data-stu-id="b1d7b-104">A callback function used to notify the host about which frames have offline analysis reports available.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d7b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1d7b-105">Syntax</span></span>


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a><span data-ttu-id="b1d7b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1d7b-106">Parameters</span></span>

<span data-ttu-id="b1d7b-107">*нумфрамесвисрепортс* </span><span class="sxs-lookup"><span data-stu-id="b1d7b-107">*numFramesWithReports* </span></span>  
<span data-ttu-id="b1d7b-108">Число кадров в count0 \_ фрамесвисрепортс.</span><span class="sxs-lookup"><span data-stu-id="b1d7b-108">The number of frames in count0\_framesWithReports.</span></span>

<span data-ttu-id="b1d7b-109">*count0 \_ фрамесвисрепортс* </span><span class="sxs-lookup"><span data-stu-id="b1d7b-109">*count0\_framesWithReports* </span></span>  
<span data-ttu-id="b1d7b-110">Массив, содержащий номера кадров кадров, для которых доступны отчеты автономного анализа.</span><span class="sxs-lookup"><span data-stu-id="b1d7b-110">An array containing the frame numbers of the frames that have offline analysis reports available.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1d7b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1d7b-111">Return value</span></span>

<span data-ttu-id="b1d7b-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b1d7b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1d7b-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1d7b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d7b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b1d7b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b1d7b-115">Header</span><span class="sxs-lookup"><span data-stu-id="b1d7b-115">Header</span></span></p></td><td><span data-ttu-id="b1d7b-116">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="b1d7b-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b1d7b-117"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="b1d7b-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b1d7b-118">**иоффлинеаналисискачекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b1d7b-118">**IOfflineAnalysisCacheCallback**</span></span>](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
