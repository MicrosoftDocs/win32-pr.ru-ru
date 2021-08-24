---
title: Жетволумеоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетволумеасинк.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетволумеоператион
- API потоковой передачи мультимедиа интерфейса Жетволумеоператион, метод Results
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e58188a0d8b0d2ed13a9cb7d7486f440f4a1303ca32208371690965f976339d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011854"
---
# <a name="getvolumeoperationgetresults-method"></a>Жетволумеоператион. results, метод

Возвращает результаты асинхронной операции, запущенной [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Том. Значение от 0 до 100. 0 указывает на минимальный том, а 100 — на максимальный.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getvolumeoperation-completed.md) .

## <a name="see-also"></a>См. также

<dl> <dt>

[**жетволумеоператион**](getvolumeoperation.md)
</dt> </dl>

 

