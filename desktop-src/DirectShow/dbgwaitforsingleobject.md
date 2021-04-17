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
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679976"
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
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ожидания отладки](wait-debugging-functions.md)
</dt> </dl>

 

 




