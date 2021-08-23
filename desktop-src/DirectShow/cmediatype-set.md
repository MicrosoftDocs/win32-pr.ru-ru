---
description: Метод Кмедиатипе. Set (Мтипе. h) задает тип носителя с другого типа носителя. Метод использует параметр "кмтипе".
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Метод Кмедиатипе. Set (Мтипе. h) — кмтипе [ref]
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a317b23b4870ad6e68032ed23f846a81019be358974ebbe75e2a5859db71303
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585884"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a>Метод Кмедиатипе. Set (Мтипе. h) — кмтипе [ref]

`Set`Метод задает тип мультимедиа из другого типа мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кмтипе* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на объект [**кмедиатипе**](cmediatype.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает S \_ OK или E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Этот метод копирует весь тип мультимедиа из *кмтипе*.

## <a name="requirements"></a>Requirements (Требования)

| Требование                   | Значение                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок  | мтипе. h (включает Потоки. h)                                                                                     |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




