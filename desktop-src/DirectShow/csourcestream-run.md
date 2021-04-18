---
description: Метод Run сообщает поток потоковой передачи для выполнения.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Метод Ксаурцестреам. Run (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679828"
---
# <a name="csourcestreamrun-method"></a>Ксаурцестреам. Run, метод

`Run`Метод оповещает поток потоковой передачи о выполнении.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Run();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Непредвиденное значение: S \_ (ОК или E) \_ .

## <a name="remarks"></a>Комментарии

В базовом классе этот метод действует так же, как запрос [**ксаурцестреам::P Аусе**](csourcestream-pause.md) , и не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




