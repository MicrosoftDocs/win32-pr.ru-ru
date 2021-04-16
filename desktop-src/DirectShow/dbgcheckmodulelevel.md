---
description: Функция Дбгчеккмодулелевел проверяет, включено ли ведение журнала для заданных типов сообщений и уровня. Игнорируется в розничных сборках.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Функция Дбгчеккмодулелевел (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679869"
---
# <a name="dbgcheckmodulelevel-function"></a>Функция Дбгчеккмодулелевел

`DbgCheckModuleLevel`Функция проверяет, включено ли ведение журнала для заданных типов сообщений и уровня. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
BOOL DbgCheckModuleLevel(
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

Уровень ведения журнала

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если ведение журнала для любого из указанных типов сообщений установлено на указанный уровень или выше. В противном случае возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




