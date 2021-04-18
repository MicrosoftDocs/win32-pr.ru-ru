---
description: Вычисляет выражение и вызывает исключение точки останова, если выражение имеет значение FALSE. Текст выражения, имя исходного файла и номер строки записываются с помощью макроса Дбглог. Игнорируется в розничных сборках.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Макрос КАССЕРТ (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680001"
---
# <a name="kassert-macro"></a>Макрос КАССЕРТ

Вычисляет выражение и вызывает исключение точки останова, если выражение имеет **значение false**. Текст выражения, имя исходного файла и номер строки записываются с помощью макроса [**дбглог**](dbglog.md) . Игнорируется в розничных сборках.

## <a name="syntax"></a>Синтаксис


```C++
void KASSERT(
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

В отличие от макроса [**Assert**](assert.md) и [**Execute \_ Assert**](execute-assert.md) , этот макрос не отображает окно сообщения с запросом пользователя. В отладочных сборках, если выражение имеет **значение false**, макрос автоматически вызывает исключение точки останова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы Assert и точка останова](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




