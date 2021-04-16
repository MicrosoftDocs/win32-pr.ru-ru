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
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657126"
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

## <a name="remarks"></a>Комментарии

В отладочных сборках функции [**дбгваитформултиплеобжектс**](dbgwaitformultipleobjects.md) и [**дбгваитфорсинглеобжект**](dbgwaitforsingleobject.md) используют это значение в качестве интервала времени ожидания.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ожидания отладки](wait-debugging-functions.md)
</dt> </dl>

 

 




