---
description: Сведения о методе Кмедиатипе. Кмедиатипе (Мтипе. h). Этот метод использует параметр "мажортипе".
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметр мажортипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073998"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметр мажортипе

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*мажортипе* 
</dt> <dd>

Указатель на **идентификатор GUID** основного типа. Конструктор инициализирует это значение GUID основного типа.

</dd> </dl>

## <a name="remarks"></a>Remarks

Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.

## <a name="requirements"></a>Requirements (Требования)

| Требование                   | Значение                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок  | мтипе. h (включает Потоки. h)                                                                                     |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




