---
description: Проверяет, имеет ли вызывающий процесс доступ на запись к блоку памяти. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: Макрос Валидатевритептр (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e7c955f31cf9e0bf1050c52b680dfc9b32741bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669390"
---
# <a name="validatewriteptr-macro"></a>Макрос Валидатевритептр

Проверяет, имеет ли вызывающий процесс доступ на запись к блоку памяти. В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .

> [!Note]  
> Этот макрос не рекомендуется к использованию. В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.

 

## <a name="syntax"></a>Синтаксис


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Указатель на блок памяти.

</dd> <dt>

*CB* 
</dt> <dd>

Размер блока памяти в байтах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот макрос не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот макрос игнорируется, если \_ при включении файла заголовков базового класса DirectShow не определена Отладка, отладка или вфвробуст. Этот макрос может существенно постоить в производительности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вксдебуг. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы проверки указателя](pointer-validation-macros.md)
</dt> </dl>

 

 




