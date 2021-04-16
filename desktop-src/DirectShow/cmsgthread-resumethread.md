---
description: 'Использует функцию Microsoft Win32 Ресумесреад для продолжения работы рабочего потока после предыдущего вызова функции-члена Кмсгсреад:: Суспендсреад.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Кмсгсреад. Ресумесреад, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679991"
---
# <a name="cmsgthreadresumethread-method"></a>Кмсгсреад. Ресумесреад, метод

Использует функцию Microsoft Win32 **ресумесреад** для продолжения работы рабочего потока после предыдущего вызова функции-члена [**Кмсгсреад:: суспендсреад**](cmsgthread-suspendthread.md) .

## <a name="syntax"></a>Синтаксис


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если функция-член выполнена, возвращаемое значение является предыдущим счетчиком приостановок потока. Если функция-член завершается ошибкой, возвращается значение 0xFFFFFFFF. Чтобы получить расширенные сведения об ошибке, вызовите функцию Microsoft Win32 **GetLastError** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мсгсрд. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




