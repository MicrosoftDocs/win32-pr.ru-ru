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
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700861"
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



 

## <a name="remarks"></a>Комментарии

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](getvolumeoperation-completed.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетволумеоператион**](getvolumeoperation.md)
</dt> </dl>

 

