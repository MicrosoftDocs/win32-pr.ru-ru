---
description: Макрос NAME создает строку только для отладки.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: ИМЯ (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688832"
---
# <a name="name"></a>ИМЯ

Макрос **Name** создает строку только для отладки.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*стрлитерал*
</dt> <dd>

Текстовая строка.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В отладочных сборках этот макрос эквивалентен **текстовому** макросу. В розничных сборках она разрешается в (TCHAR \* ) **null**. Этот макрос полезен при объявлении имени объекта, производного от класса [**кбасеобжект**](cbaseobject.md) .


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




