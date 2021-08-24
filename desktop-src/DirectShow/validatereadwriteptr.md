---
description: Проверяет, что вызывающий процесс имеет доступ на чтение и запись к блоку памяти. В противном случае макрос вызывает макрос Дбгбреак.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Макрос Валидатереадвритептр (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ec4d1c0440d0747024efadaa441ca062da512283f5a01f29be12b19c0f7c0567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755664"
---
# <a name="validatereadwriteptr-macro"></a>Макрос Валидатереадвритептр

Проверяет, что вызывающий процесс имеет доступ на чтение и запись к блоку памяти. В противном случае макрос вызывает макрос [**дбгбреак**](dbgbreak.md) .

> [!Note]  
> Этот макрос не рекомендуется к использованию. в Windows SDK для Windows Vista (и более поздних версий) этот макрос не выполняет никаких действий.

 

## <a name="syntax"></a>Синтаксис


```C++
void ValidateReadWritePtr(
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

## <a name="remarks"></a>Remarks

этот макрос игнорируется, если \_ при включении файла заголовка DirectShow базового класса не определена отладка, отладка или вфвробуст. Этот макрос может существенно постоить в производительности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>вксдебуг. h (включает Потоки. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы проверки указателя](pointer-validation-macros.md)
</dt> </dl>

 

 




