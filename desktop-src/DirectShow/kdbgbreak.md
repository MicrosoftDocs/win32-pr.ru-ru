---
description: Вызывает исключение точки останова и записывает в журнал указанную строку с помощью макроса Дбглог. Игнорируется в розничных сборках.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Макрос Кдбгбреак (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685135"
---
# <a name="kdbgbreak-macro"></a>Макрос Кдбгбреак

Вызывает исключение точки останова и записывает в журнал указанную строку с помощью макроса [**дбглог**](dbglog.md) . Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стрлитерал* 
</dt> <dd>

Текстовая строка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот макрос не возвращает значение.

## <a name="remarks"></a>Комментарии

В отличие от макроса [**дбгбреак**](dbgbreak.md) , этот макрос не отображает окно сообщения с запросом пользователя. В отладочных сборках это автоматически приводит к возникновению исключения точки останова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы Assert и точка останова](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




