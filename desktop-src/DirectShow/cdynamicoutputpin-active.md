---
description: Кдинамикаутпутпин. Active Method — активный метод уведомляет ПИН-код о том, что фильтр активен.
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
ms.openlocfilehash: 12e59b434562e84c42228c16282620efe10866ea9dad85a4d62beb46f5a59e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688984"
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



 

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасеаутпутпин:: Active**](cbaseoutputpin-active.md) . Он сбрасывает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) . Если фильтр-владелец не вызвал **сетконфигинфо**, этот метод возвращает значение E \_ Fail.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




