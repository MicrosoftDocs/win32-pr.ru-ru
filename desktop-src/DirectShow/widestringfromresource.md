---
description: Функция Видестрингфромресаурце загружает строку расширенных символов из файла ресурсов с заданным идентификатором ресурса.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Функция Видестрингфромресаурце (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668736"
---
# <a name="widestringfromresource-function"></a>Функция Видестрингфромресаурце

`WideStringFromResource`Функция загружает строку расширенных символов из файла ресурсов с заданным идентификатором ресурса.

## <a name="syntax"></a>Синтаксис


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
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

Страницы свойств обычно вызываются через интерфейсы COM, которые используют строки расширенных символов независимо от того, как создается двоичный файл. Эта функция позволяет преобразовать строку ресурса в строку расширенных символов. Функция преобразует ресурс в строку расширенных символов (если она еще не одна) после ее загрузки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные функции страницы свойств](property-page-helper-functions.md)
</dt> </dl>

 

 




