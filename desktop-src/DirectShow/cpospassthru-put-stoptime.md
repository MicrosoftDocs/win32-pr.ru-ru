---
description: Метод размещения \_ StopTime задает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод Имедиапоситион::p UT \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Метод CPosPassThru.put_StopTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d91d49f2517a3d3b9efc50d70ace1b75562b50df8acda7c48826e7c088439928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055094"
---
# <a name="cpospassthruput_stoptime-method"></a>Кпоспасссру. размещение \_ метода StopTime

`put_StopTime`Метод задает время, когда воспроизведение будет останавливаться, относительно длительности потока. Этот метод реализует метод [**имедиапоситион::p UT \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ллтиме* 
</dt> <dd>

Время окончания в секундах. 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




