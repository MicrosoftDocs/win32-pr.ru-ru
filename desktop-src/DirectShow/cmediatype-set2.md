---
description: Метод Set задает тип мультимедиа из другого типа носителя.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Метод Кмедиатипе. Set (Мтипе. h)
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
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665297"
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

## <a name="remarks"></a>Комментарии

Этот метод копирует весь тип мультимедиа из *мтипе*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




