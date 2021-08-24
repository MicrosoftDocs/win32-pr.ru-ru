---
description: Функция Стрингфромресаурце загружает строку из файла ресурсов с заданным идентификатором ресурса.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Функция Стрингфромресаурце (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a12bffb3659bd18f630ce3ff06435a701ed77f8fba2af79b20df6d6b2574ad8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329654"
---
# <a name="stringfromresource-function"></a>Функция Стрингфромресаурце

`StringFromResource`Функция загружает строку из файла ресурсов с заданным идентификатором ресурса.

## <a name="syntax"></a>Синтаксис


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pBuffer* 
</dt> <dd>

Указатель на строку, соответствующую *иресаурцеид*.

</dd> <dt>

*иресаурцеид* 
</dt> <dd>

Идентификатор ресурса извлекаемой строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ту же строку, что и *pBuffer*. Если функция не выполнена успешно, возвращает пустую строку.

## <a name="remarks"></a>Remarks

Буфер *pBuffer* должен иметь длину не менее str \_ \_ байт.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции страницы свойств](property-page-helper-functions.md)
</dt> </dl>

 

 




