---
description: Метод Set задает тип мультимедиа из другого типа носителя.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Метод Кмедиатипе. Set (Мтипе. h) — мтипе [ref]
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
ms.openlocfilehash: 350e88cefa7c0f5f6946218d220fcad4a118cf53e203a68eeb9f75c0d0eace1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156067"
---
# <a name="cmediatypeset-method-mtypeh"></a>Метод Кмедиатипе. Set (Мтипе. h)

`Set`Метод задает тип мультимедиа из другого типа мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*мтипе* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает S \_ OK или E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Этот метод копирует весь тип мультимедиа из *мтипе*.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




