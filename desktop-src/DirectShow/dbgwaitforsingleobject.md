---
description: Ожидает, пока объект станет сигнальным.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Функция Дбгваитфорсинглеобжект (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5e8180c905cdb7d8d1024f22a85984c17c0e12e18971499d29ed1479a79498f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749354"
---
# <a name="dbgwaitforsingleobject-function"></a>Функция Дбгваитфорсинглеобжект

Ожидает, пока объект станет сигнальным.

В отладочной сборке эта функция активирует утверждение, если интервал времени ожидания истекает до получения сигнала от объекта. Чтобы установить интервал времени ожидания, вызовите функцию [**дбгсетваиттимеаут**](dbgsetwaittimeout.md) .

В розничной сборке эта функция эквивалентна функции **WaitForSingleObject** с интервалом времени ожидания, равным бесконечности.

## <a name="syntax"></a>Синтаксис


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*h* 
</dt> <dd>

Обработчик для объекта.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ожидания отладки](wait-debugging-functions.md)
</dt> </dl>

 

 




