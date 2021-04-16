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
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679760"
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

## <a name="remarks"></a>Комментарии

Буфер *pBuffer* должен иметь длину не менее str \_ \_ байт.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции страницы свойств](property-page-helper-functions.md)
</dt> </dl>

 

 




