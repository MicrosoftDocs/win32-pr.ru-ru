---
description: Проверяет, имеет ли вызывающий процесс доступ на чтение к строке расширенных символов. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Макрос Валидатестрингптрв (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689456"
---
# <a name="validatestringptrw-macro"></a>Макрос Валидатестрингптрв

Проверяет, имеет ли вызывающий процесс доступ на чтение к строке расширенных символов. В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .

> [!Note]  
> Этот макрос не рекомендуется к использованию. В Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.

 

## <a name="syntax"></a>Синтаксис


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Указатель на строку расширенных символов, заканчивающуюся НУЛЕМ.

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

 

 




