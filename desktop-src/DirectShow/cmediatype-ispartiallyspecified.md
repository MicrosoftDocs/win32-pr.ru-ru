---
description: Метод ИспартиаллиспеЦифиед определяет, определен ли тип мультимедиа частично. Тип мультимедиа является разделяемым, если основной тип, подтип или тип формата имеют \_ значение GUID null.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Кмедиатипе. ИспартиаллиспеЦифиед, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676010"
---
# <a name="cmediatypeispartiallyspecified-method"></a>Кмедиатипе. ИспартиаллиспеЦифиед, метод

`IsPartiallySpecified`Метод определяет, определен ли тип мультимедиа частично. Тип мультимедиа является *разделяемым* , если основной тип, подтип или тип формата имеют \_ значение GUID null.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если тип мультимедиа указан частично. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Комментарии

Метод [**Ипин:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) может принимать частичные типы мультимедиа.

Реализация фактически не тестирует подтип. Если существует указанный тип формата, тип мультимедиа не считается частичным, даже если его подтип имеет \_ значение GUID null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




