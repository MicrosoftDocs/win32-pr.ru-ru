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
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665472"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




