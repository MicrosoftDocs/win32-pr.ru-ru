---
description: Запросы на запуск автономного анализа с указанным источником, манифестом, параметрами и указанным кадром.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иоффлинеаналисисрекуест:: Рекуестоффлинеаналисисасинк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85243b1c07db1f2c30a4e29b221582fd507360f1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624340"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Метод Иоффлинеаналисисрекуест:: Рекуестоффлинеаналисисасинк

Запросы на запуск автономного анализа с указанным источником, манифестом, параметрами и указанным кадром.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a>Параметры

*аналисиссаурце*   
Спекфиес, где источник анализа получен из кэшированных отчетов или из воспроизведения.

*манифестксмл*   
Строка COM, содержащая путь к XML-файлу манифеста.

*параметерсксмл*   
Строка COM, содержащая путь к XML-файлу параметров.

*"*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*каптурефуллфиленаме*   
Строка COM, содержащая абсолютный путь к файлу записи (. vsglog).

*фраменумбер*   
Указанный кадр.

*аутпутфуллфиленаме*   
Строка COM, содержащая абсолютный путь к файлу, в который записываются выходные данные.

*рекуесткаллбакк*   
Адрес обратного вызова, используемый для уведомления узла о результатах.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иоффлинеаналисисрекуест**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
