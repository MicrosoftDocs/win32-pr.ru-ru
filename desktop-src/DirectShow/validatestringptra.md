---
description: Проверяет, имеет ли вызывающий процесс доступ на чтение к строке ANSI. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Макрос Валидатестрингптра (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679982"
---
# <a name="validatestringptra-macro"></a>Макрос Валидатестрингптра

Проверяет, имеет ли вызывающий процесс доступ на чтение к строке ANSI. В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .

> [!Note]  
> Этот макрос не рекомендуется к использованию. В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.

 

## <a name="syntax"></a>Синтаксис


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Указатель на строку ANSI, заканчивающуюся нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот макрос не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот макрос игнорируется, если \_ при включении файла заголовков базового класса DirectShow не определена Отладка, отладка или вфвробуст.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы проверки указателя](pointer-validation-macros.md)
</dt> </dl>

 

 




