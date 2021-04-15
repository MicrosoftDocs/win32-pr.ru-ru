---
description: Активный метод уведомляет ПИН-код о том, что фильтр активен.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Метод Кдинамикаутпутпин. Active (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669431"
---
# <a name="cdynamicoutputpinactive-method"></a>Кдинамикаутпутпин. активный метод

`Active`Метод уведомляет ПИН-код о том, что фильтр активен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Active();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                            | Описание                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                                                                                             |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Ошибка. [**Кдинамикаутпутпин:: сетконфигинфо**](cdynamicoutputpin-setconfiginfo.md) не был вызван.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) . Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) . Если фильтр-владелец не вызвал **сетконфигинфо**, этот метод возвращает значение E \_ Fail.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




