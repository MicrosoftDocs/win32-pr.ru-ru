---
title: Жетмутеоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетмутеасинк.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетмутеоператион
- API потоковой передачи мультимедиа интерфейса Жетмутеоператион, метод Results
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37b8356a677f5e752fdf4e4ec658cc4077a17fa76b6181097d5753d898eef89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972413"
---
# <a name="getmuteoperationgetresults-method"></a>Жетмутеоператион. results, метод

Возвращает результаты асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Значение выключения. Значение true указывает, что звук в данный момент выключен. Значение false указывает, что звук не отключен.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getmuteoperation-completed.md) .

## <a name="see-also"></a>См. также

<dl> <dt>

[**жетмутеоператион**](getmuteoperation.md)
</dt> </dl>

 

