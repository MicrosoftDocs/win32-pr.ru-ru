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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674770"
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

## <a name="remarks"></a>Комментарии

Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.

## <a name="requirements"></a>Требования

| Требование                   | Значение                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Мтипе. h (включение Streams. h)                                                                                     |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




