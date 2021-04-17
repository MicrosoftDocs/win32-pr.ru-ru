---
description: Метод Чекктиме определяет, вызвано ли указанное время.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Ккмдкуеуе. Чекктиме, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680014"
---
# <a name="ccmdqueuechecktime-method"></a>Ккмдкуеуе. Чекктиме, метод

`CheckTime`Метод определяет, вызвано ли указанное время.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*time* 
</dt> <dd>

Время для проверки.

</dd> <dt>

*бстреам* 
</dt> <dd>

**Значение true** , если параметр *времени* является значением потокового времени; Значение **false** , если *время* является значением времени презентации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если указанное время еще не прошло.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




