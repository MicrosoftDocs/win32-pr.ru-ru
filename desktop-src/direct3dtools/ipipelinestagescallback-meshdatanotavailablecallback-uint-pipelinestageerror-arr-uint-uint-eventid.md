---
description: Обратный вызов, уведомляющий узел о том, какие этапы конвейера не могут вернуть данные сетки для события, указанного в связанном запросе.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataNotAvailableCallback\_UINT\_PipeLineStageError\_arr\_UINT\_UINT\_EventID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ипипелинестажескаллбакк:: Мешдатанотаваилаблекаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A51E7C45-C1F0-4576-8638-9C3B185385BA
api_name:
- IPipeLineStagesCallback.MeshDataNotAvailableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9c95f661c5a18f2573fe477f3aa1ef4d0035ee1e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622140"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventidspanipipelinestagescallbackmeshdatanotavailablecallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatanotavailablecallback_uint_pipelinestageerror_arr_uint_uint_eventid"></span>Метод Ипипелинестажескаллбакк:: Мешдатанотаваилаблекаллбакк

Обратный вызов, уведомляющий узел о том, какие этапы конвейера не могут вернуть данные сетки для события, указанного в связанном запросе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MeshDataNotAvailableCallback(
   UINT                  numberStages,
   PipeLineStageError [] count0_errors,
   UINT                  width,
   UINT                  height,
   EventID               eid
);
```

## <a name="parameters"></a>Параметры

*нумберстажес*   
Число возвращенных ошибок этапа.

*\_ошибки count0*   
Ошибки этапа конвейера.

*Ширина*   
Ширина цепочки подкачки, связана с вызовом Draw. Используется при запросе изображений предварительного просмотра конвейера.

*равно*   
Высота цепочки подкачки, связана с вызовом Draw. Используется при запросе изображений предварительного просмотра конвейера.

*Аль*   
Событие, представленное в результатах.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ипипелинестажескаллбакк**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
