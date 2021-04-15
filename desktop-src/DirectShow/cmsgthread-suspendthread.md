---
description: Использует функцию Microsoft Win32 Суспендсреад для приостановки работы выполняющегося потока.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Кмсгсреад. Суспендсреад, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669394"
---
# <a name="cmsgthreadsuspendthread-method"></a>Кмсгсреад. Суспендсреад, метод

Использует функцию Microsoft Win32 **суспендсреад** для приостановки работы выполняющегося потока.

## <a name="syntax"></a>Синтаксис


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если функция-член выполнена, возвращаемое значение является предыдущим счетчиком приостановок потока. Если функция-член завершается ошибкой, возвращается значение 0xFFFFFFFF. Чтобы получить расширенные сведения об ошибке, вызовите функцию Microsoft Win32 **GetLastError** .

## <a name="remarks"></a>Комментарии

Клиентский поток вызывает эту функцию члена для приостановки работы рабочего потока. Рабочий поток остается приостановленным и не будет выполняться до выполнения дополнительного вызова функции-члена [**кмсгсреад:: ресумесреад**](cmsgthread-resumethread.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мсгсрд. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




