---
title: Плайбаккоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной одним из методов воспроизведения Медиарендерер.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Плайбаккоператион
- API потоковой передачи мультимедиа интерфейса Плайбаккоператион, метод Results
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411555"
---
# <a name="playbackoperationgetresults-method"></a>Плайбаккоператион. results, метод

Возвращает результаты асинхронной операции, запущенной одним из методов воспроизведения [**медиарендерер**](mediarenderer.md) .

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

Результат операции. Значение 0 указывает, что операция завершена. Другие значения зарезервированы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Метод " **Results** " обычно вызывается из обработчика событий, зарегистрированного путем установки свойства [**Completed**](playbackoperation-completed.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**плайбаккоператион**](playbackoperation.md)
</dt> </dl>

 

 





