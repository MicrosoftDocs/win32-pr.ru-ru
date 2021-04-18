---
description: Метод Бегинфлуш информирует фильтр-владелец о необходимости сброса нисходящих фильтров. Производный класс должен реализовывать этот метод.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Кпуллпин. Бегинфлуш, метод (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675589"
---
# <a name="cpullpinbeginflush-method"></a>Кпуллпин. Бегинфлуш, метод

`BeginFlush`Метод информирует фильтр-владелец о необходимости сброса нисходящих фильтров. Производный класс должен реализовывать этот метод.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Метод [**кпуллпин:: Seek**](cpullpin-seek.md) вызывает этот метод. Реализуйте этот метод, чтобы вызвать метод [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) для каждого нисходящиго входного ПИН-кода, получающего данные от этого объекта. Если закрепление вывода фильтра является производным от [**кбасеаутпутпин**](cbaseoutputpin.md), вызовите метод [**Кбасеаутпутпин::D еливербегинфлуш**](cbaseoutputpin-deliverbeginflush.md) .

Такая схема позволяет фильтровать поиск в потоке, просто вызывая метод **Seek** для объекта **кпуллпин** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




