---
description: Задает значение времени ожидания отладки. Игнорируется в розничных сборках.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Функция Дбгсетваиттимеаут (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67a5522184b9e88cd4b8ac9f23246f96c13ffad2175d625334de32d34c750e12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654026"
---
# <a name="dbgsetwaittimeout-function"></a>Функция Дбгсетваиттимеаут

Задает значение времени ожидания отладки. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двтимеаут* 
</dt> <dd>

Значение времени ожидания в миллисекундах или бесконечно, чтобы неограниченное время ожидания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

В отладочных сборках функции [**дбгваитформултиплеобжектс**](dbgwaitformultipleobjects.md) и [**дбгваитфорсинглеобжект**](dbgwaitforsingleobject.md) используют это значение в качестве интервала времени ожидания.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ожидания отладки](wait-debugging-functions.md)
</dt> </dl>

 

 




