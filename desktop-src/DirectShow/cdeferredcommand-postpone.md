---
description: Метод отсрочки задает новое время презентации для ранее поставленной в очередь команды.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Метод Кдеферредкомманд. отсрочки (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680081"
---
# <a name="cdeferredcommandpostpone-method"></a>Кдеферредкомманд. Отсрочка метода

`Postpone`Метод задает новое время презентации для ранее поставленной в очередь команды.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*невтиме* 
</dt> <dd>

Новое время презентации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ электронное \_ время \_ VFW \_ , которое уже прошло, если *невтиме* уже передан. В противном случае возвращает **значение HRESULT** , полученное в результате вызова метода [**ккмдкуеуе:: reinsert**](ccmdqueue-remove.md) (при извлечении из списка) или [**ккмдкуеуе:: INSERT**](ccmdqueue-insert.md) (при повторной вставке с измененным временем).

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**идеферредкомманд::P остпоне**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




