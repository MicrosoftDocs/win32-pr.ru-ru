---
description: Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h) — параметр мтипе'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b5960ac5f9dc3e685aa0b8b281989185580fd5b683392aaf93a0891d0ebaa35d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016271"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>Кмедиатипе. Кмедиатипе:: operator = метод (Мтипе. h)

Этот оператор перегружает оператор присваивания для копирования типа мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
CMediaType& CMediaType::operator=(
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

Возвращает ссылку на объект.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




