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
ms.openlocfilehash: c13463ae4effb9fee31ad7c9201ad5af6fd406099c5259c2e6fdff9dcbb62798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814194"
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



 

## <a name="remarks"></a>Remarks

Этот метод вызывает метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) для входного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




