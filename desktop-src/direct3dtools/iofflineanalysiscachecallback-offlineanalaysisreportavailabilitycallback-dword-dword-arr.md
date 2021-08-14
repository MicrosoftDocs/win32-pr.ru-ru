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
ms.openlocfilehash: ec2d874f06bb850538579edc29f5caa289d6f163846eff0657d49a41becc8f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721865"
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

## <a name="requirements"></a>Requirements (Требования)

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иоффлинеаналисискачекаллбакк**](/windows/desktop/direct3dtools/iofflineanalysiscachecallback)

 

 
