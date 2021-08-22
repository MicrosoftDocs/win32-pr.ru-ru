---
description: Метод Сетсубтипе задает подтип.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Кмедиатипе. Сетсубтипе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96445074ce2f0cc5a27a4988087f2fd910444beca88e5dc89c84585a8a98b338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566374"
---
# <a name="cmediatypesetsubtype-method"></a>Кмедиатипе. Сетсубтипе, метод

`SetSubtype`Метод задает подтип.

## <a name="syntax"></a>Синтаксис


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псубтипе* 
</dt> <dd>

Указатель на **идентификатор GUID** , указывающий подтип.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




