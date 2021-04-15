---
description: Метод Дисплайпининфо отслеживает подключение ПИН-кода во время отладки.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Кбасепин. Дисплайпининфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668772"
---
# <a name="cbasepindisplaypininfo-method"></a>Кбасепин. Дисплайпининфо, метод

`DisplayPinInfo`Метод отслеживает подключение ПИН-кода во время отладки.

## <a name="syntax"></a>Синтаксис


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прецеивепин* 
</dt> <dd>

Указатель на принимающий ПИН-код.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

В отладочных сборках этот метод вызывает функцию [**дбглог**](dbglog.md) для трассировки попытки соединения. В розничных сборках этот метод не выполняет никаких действий.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




