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
ms.openlocfilehash: 9d1f32dd20cde915fabce8a1ec805d5d79499349
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624190"
---
# <a name="span-idvspixengineiofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptrspaniofflineanalysiscacherequestrequestofflineanalysisreportavailabilityasync-method"></a><span id="vspixengine.iofflineanalysiscacherequest_requestofflineanalysisreportavailabilityasync_dword_dword_arr_iofflineanalysiscachecallback_ptr"></span>Метод Иоффлинеаналисискачерекуест:: Рекуестоффлинеаналисисрепортаваилабилитясинк

Запросы на кэширование автономного отчета об анализе указанных кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestOfflineAnalysisReportAvailabilityAsync(
   DWORD                           numFrames,
   DWORD []                        count0_frameNumbers,
   IOfflineAnalysisCacheCallback * requestCallback
);
```

## <a name="parameters"></a>Параметры

*нумфрамес*   
Число кадров, для которых формируются отчеты об анализе.

*count0 \_ фраменумберс*   
Указанные кадры.

*рекуесткаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иоффлинеаналисискачерекуест**](/windows/desktop/direct3dtools/iofflineanalysiscacherequest)

 

 
