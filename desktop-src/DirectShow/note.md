---
description: Макрос примечания отправляет строку в расположение выходных данных отладки. Игнорируется в розничных сборках.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Примечание (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0becacba37f3f474577c36a694539de77795f1c19ccf3b1655cb80370be9e297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050924"
---
# <a name="note"></a>ПРИМЕЧАНИЕ

`NOTE`Макрос отправляет строку в расположение выходных данных отладки. Игнорируется в розничных сборках.

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*пформат*
</dt> <dd>

Строка формата в стиле printf.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*—*arg5*
</dt> <dd>

Дополнительные аргументы для строки формата. Число аргументов должно совпадать с именем макроса. Например, **Note1** принимает один аргумент, а **NOTE5** принимает пять аргументов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эти макросы являются вариантами макроса [**дбглог**](dbglog.md) . Они создают сообщения трассировки журнала уровня 5 \_ .

## <a name="example"></a>Пример


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Выходные функции отладки](debug-output-functions.md)
</dt> </dl>

 

 




