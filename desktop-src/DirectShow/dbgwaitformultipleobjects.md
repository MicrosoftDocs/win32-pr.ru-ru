---
description: Ожидает сигнала для всех (или всех) указанных объектов.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Функция Дбгваитформултиплеобжектс (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658031"
---
# <a name="dbgwaitformultipleobjects-function"></a>Функция Дбгваитформултиплеобжектс

Ожидает сигнала для всех (или всех) указанных объектов.

В отладочной сборке эта функция активирует утверждение, если интервал времени ожидания истекает до того, как объекты будут сигнальными. Чтобы установить интервал времени ожидания, вызовите функцию [**дбгсетваиттимеаут**](dbgsetwaittimeout.md) .

В розничной сборке эта функция эквивалентна функции **WaitForMultipleObjects** с интервалом времени ожидания, равным бесконечности.

## <a name="syntax"></a>Синтаксис


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нкаунт* 
</dt> <dd>

Число объектов.

</dd> <dt>

*лфандлес* 
</dt> <dd>

Массив дескрипторов объектов размером *нкаунт*.

</dd> <dt>

*бваиталл* 
</dt> <dd>

Логическое значение, указывающее, следует ли ожидать все объекты. Если **значение равно true**, функция ожидает получения сигнала для всех объектов. В противном случае он ожидает сигнала хотя бы для одного объекта.

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

 

 




