---
description: Метод Сеттипе задает основной тип.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Кмедиатипе. Сеттипе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37d035202d4674da11016620dc3c3d1ba3ab99f6ca514b9581f7dd2e4d9592d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954393"
---
# <a name="cmediatypesettype-method"></a>Кмедиатипе. Сеттипе, метод

`SetType`Метод задает основной тип.

## <a name="syntax"></a>Синтаксис


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птипе* 
</dt> <dd>

Указатель на **идентификатор GUID** , указывающий основной тип.

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

 

 




