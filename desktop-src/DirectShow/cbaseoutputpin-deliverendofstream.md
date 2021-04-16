---
description: Метод Деливерендофстреам доставляет уведомление в виде конца потока в подключенный входной ПИН-код.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Кбасеаутпутпин. Деливерендофстреам, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657886"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>Кбасеаутпутпин. Деливерендофстреам, метод

`DeliverEndOfStream`Метод доставляет уведомление о завершении потока в подключенный входной ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                           | Описание                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>              |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | ПИН-код не подключен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




