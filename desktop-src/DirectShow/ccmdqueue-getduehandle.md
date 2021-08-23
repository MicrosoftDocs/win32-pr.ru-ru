---
description: Метод Жетдуехандле извлекает дескриптор события для получения сигнала.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Ккмдкуеуе. Жетдуехандле, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62fbe0e38e24891add93e63e0c03d521289ed345078e8e567a376e9bd639d997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016422"
---
# <a name="ccmdqueuegetduehandle-method"></a>Ккмдкуеуе. Жетдуехандле, метод

`GetDueHandle`Метод получает дескриптор события для получения сигнала.

## <a name="syntax"></a>Синтаксис


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер события.

## <a name="remarks"></a>Remarks

Возвращают обработчики событий при наличии отложенных команд, которые должны быть вызваны выполнением (когда [**ккмдкуеуе:: жетдуекомманд**](ccmdqueue-getduecommand.md) не будет блокироваться).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккмдкуеуе**](ccmdqueue.md)
</dt> </dl>

 

 




