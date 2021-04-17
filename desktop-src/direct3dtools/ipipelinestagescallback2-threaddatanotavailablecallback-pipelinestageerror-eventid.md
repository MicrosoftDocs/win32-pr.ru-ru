---
description: Обратный вызов, уведомляющий узел о том, что Среаддата недоступен для определенного этапа и события конвейера.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataNotAvailableCallback\_PipeLineStageError\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesCallback2:: Среаддатанотаваилаблекаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 231DC830-5F1A-4DDA-B5D0-C7FBCEDCB2A0
api_name:
- IPipeLineStagesCallback2.ThreadDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a0c9cc0bc32b6d01394be1403e961d7ae37a1d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673094"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventidspanipipelinestagescallback2threaddatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback2_threaddatanotavailablecallback_pipelinestageerror_eventid"></span>Метод IPipeLineStagesCallback2:: Среаддатанотаваилаблекаллбакк

Обратный вызов, уведомляющий узел о том, что Среаддата недоступен для определенного этапа и события конвейера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ThreadDataNotAvailableCallback(
   PipeLineStageError error,
   EventID            eid
);
```

## <a name="parameters"></a>Параметры

*план*   
Ошибка этапа конвейера.

*Аль*   
Событие, представленное в результатах.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPipeLineStagesCallback2**](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
