---
description: Функция Дбгсетмодулелевел задает уровень ведения журнала для одного или нескольких типов сообщений. Игнорируется в розничных сборках.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Функция Дбгсетмодулелевел (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06f8cccbf7212514ae9f5cbd338f4e8876137cf038992ae111e7eeb743284774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654054"
---
# <a name="dbgsetmodulelevel-function"></a>Функция Дбгсетмодулелевел

Функция **дбгсетмодулелевел** задает уровень ведения журнала для одного или нескольких типов сообщений. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Типы* 
</dt> <dd>

Побитовое сочетание одного или нескольких типов сообщений.

</dd> <dt>

*Уровень* 
</dt> <dd>

Уровень ведения журнала для указанных типов сообщений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




