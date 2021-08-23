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
ms.openlocfilehash: 079b9f1a852ff0b9eb6e1c38cea6e24e3ee00107ac46ca15e738e1ef9e0eb8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074368"
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

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**идеферредкомманд::P остпоне**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдеферредкомманд**](cdeferredcommand.md)
</dt> </dl>

 

 




