---
description: Вычисляет выражение в сборках Debug и Retail. В отладочных сборках отображает диагностическое сообщение, если выражение имеет значение FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Макрос EXECUTE_ASSERT (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652273"
---
# <a name="execute_assert-macro"></a>ВЫПОЛНИТЬ \_ макрос assert

Вычисляет выражение в сборках Debug и Retail. В отладочных сборках отображает диагностическое сообщение, если выражение имеет **значение false**.

## <a name="syntax"></a>Синтаксис


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*cond* 
</dt> <dd>

Вычисляемое выражение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот макрос не возвращает значение.

## <a name="remarks"></a>Комментарии

В отличие от макроса [**Assert**](assert.md) , этот макрос вычисляет выражение в розничных сборках. Если в отладочных сборках выражение имеет **значение false**, макрос отображает окно сообщения с текстом выражения, именем исходного файла и номером строки. Пользователь может игнорировать утверждение, ввести отладчик или выйти из приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы Assert и точка останова](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




