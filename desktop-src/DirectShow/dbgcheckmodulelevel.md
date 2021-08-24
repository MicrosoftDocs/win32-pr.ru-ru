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
ms.openlocfilehash: dd6d7c61e7989987401c22386054c02f87410ce66dbb98bb6e20a813f2c851be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823704"
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
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




