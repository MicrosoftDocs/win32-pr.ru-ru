---
description: Вычисляет выражение и отображает диагностическое сообщение, если выражение имеет значение FALSE. Игнорируется в розничных сборках.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Макрос ASSERT (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1c64ae2256ae132fccdca6e483fae3f79d28b0cda66d7701acbe95abb1222d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824433"
---
# <a name="assert-macro"></a>ASSERT - макрос

Вычисляет выражение и отображает диагностическое сообщение, если выражение имеет **значение false**. Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void ASSERT(
   BOOL cond
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

## <a name="remarks"></a>Remarks

Если в отладочных сборках выражение имеет **значение false**, этот макрос отображает окно сообщения с текстом выражения, именем исходного файла и номером строки. Пользователь может игнорировать утверждение, ввести отладчик или выйти из приложения.

## <a name="examples"></a>Примеры


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы Assert и точка останова](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




