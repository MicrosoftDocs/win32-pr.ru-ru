---
description: Метод Матчеспартиал определяет, соответствует ли этот тип носителя частично указанному типу носителя.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Кмедиатипе. Матчеспартиал, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668981"
---
# <a name="cmediatypematchespartial-method"></a>Кмедиатипе. Матчеспартиал, метод

`MatchesPartial`Метод определяет, соответствует ли этот тип носителя частично указанному типу мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппартиал* 
</dt> <dd>

Указатель на тип носителя для сопоставления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если типы мультимедиа совпадают. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Комментарии

Тип носителя, заданный параметром *ппартиал* , может иметь значение GUID \_ null для основного типа, подтипа или типа формата. Все элементы со \_ значениями NULL GUID не проверяются. (По сути, GUID \_ NULL выступает в качестве подстановочного знака.) Элементы со значениями, отличными от GUID \_ null, должны соответствовать типу носителя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




