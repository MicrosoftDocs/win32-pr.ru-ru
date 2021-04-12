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
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysisprogress_dword_doublespaniofflineanalysiscallbackofflineanalysisprogress-method"></a><span id="vspixengine.iofflineanalysiscallback_offlineanalysisprogress_dword_double"></span>Метод Иоффлинеаналисискаллбакк:: Оффлинеаналисиспрогресс

Функция обратного вызова, используемая для уведомления узла о ходе автономного анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a>Параметры

*"*   
Файл cookie, который однозначно идентифицирует запрос, и может использоваться для оповещения о том, что он должен быть отменен.

*двигается*   
Процент выполнения.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иоффлинеаналисискаллбакк**](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
