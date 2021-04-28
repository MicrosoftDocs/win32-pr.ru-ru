---
description: 'Ктрансформинпутпин. EndOfStream, метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Ктрансформинпутпин. EndOfStream, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084982"
---
# <a name="ctransforminputpinendofstream-method"></a>Ктрансформинпутпин. EndOfStream, метод

`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                           | Описание                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>                         |
| <dl> <dt>**S \_ false**</dt> </dl>               | ПИН-код в данный момент очищается.<br/>       |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | Выходной ПИН-код не подключен.<br/> |
| <dl> <dt>**\_ \_ ошибка среды выполнения VFW E \_**</dt> </dl> | Произошла ошибка времени выполнения.<br/>       |
| <dl> <dt>**VFW \_ E — \_ неправильное \_ состояние**</dt> </dl>   | ПИН-код остановлен.<br/>              |



 

## <a name="remarks"></a>Remarks

Этот метод вызывает метод [**ктрансформфилтер:: EndOfStream**](ctransformfilter-endofstream.md) фильтра для доставки уведомления конца потока.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




