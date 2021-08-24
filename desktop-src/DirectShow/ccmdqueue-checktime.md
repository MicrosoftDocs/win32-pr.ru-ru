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
ms.openlocfilehash: 826b59d12c135e9c86ce923f37e1558dca4f13efafb4880aecab1384829a484a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910434"
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
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




