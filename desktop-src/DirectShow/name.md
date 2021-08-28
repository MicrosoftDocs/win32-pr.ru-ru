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
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107685"
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

## <a name="remarks"></a>Remarks

В отладочных сборках этот макрос эквивалентен **текстовому** макросу. В розничных сборках она разрешается в (TCHAR \* ) **null**. Этот макрос полезен при объявлении имени объекта, производного от класса [**кбасеобжект**](cbaseobject.md) .


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




