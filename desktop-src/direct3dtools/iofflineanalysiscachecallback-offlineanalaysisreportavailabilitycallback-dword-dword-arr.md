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
ms.openlocfilehash: 5c7096efb91925daabd0d1c5230edfd15b04e2b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628090"
---
# <a name="span-idvspixengineiofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arrspaniofflineanalysiscachecallbackofflineanalaysisreportavailabilitycallback-method"></a><span id="vspixengine.iofflineanalysiscachecallback_offlineanalaysisreportavailabilitycallback_dword_dword_arr"></span>Метод Иоффлинеаналисискачекаллбакк:: Оффлинеаналайсисрепортаваилабилитикаллбакк

Функция обратного вызова, используемая для уведомления узла о том, какие кадры имеют доступ к автономным отчетам анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OfflineAnalaysisReportAvailabilityCallback(
   DWORD    numFramesWithReports,
   DWORD [] count0_framesWithReports
);
```

## <a name="parameters"></a>Параметры

*нумфрамесвисрепортс*   
Число кадров в count0 \_ фрамесвисрепортс.

*count0 \_ фрамесвисрепортс*   
Массив, содержащий номера кадров кадров, для которых доступны отчеты автономного анализа.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иоффлинеаналисискачекаллбакк**](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
