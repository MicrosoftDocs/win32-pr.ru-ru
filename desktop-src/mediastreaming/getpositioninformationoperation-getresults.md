---
title: Жетпоситионинформатионоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетпоситионинформатионасинк.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетпоситионинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жетпоситионинформатионоператион, метод Results
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e924227c37318a788f9c30aea5e5125a40c69175ac7c4449a54ebcc4cf61326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721064"
---
# <a name="getpositioninformationoperationgetresults-method"></a>Жетпоситионинформатионоператион. results, метод

Возвращает результаты асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Ссылка на структуру [**поситионинформатион**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) , которая содержит результаты операции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getpositioninformationoperation-completed.md) .

## <a name="see-also"></a>См. также

<dl> <dt>

[**жетпоситионинформатионоператион**](getpositioninformationoperation.md)
</dt> </dl>

 

