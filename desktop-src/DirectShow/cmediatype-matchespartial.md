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
ms.openlocfilehash: a6049ad4526d8776b25e81fe4d75b727196f8fa1251a1959662cca71b161fbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073978"
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

## <a name="remarks"></a>Remarks

Тип носителя, заданный параметром *ппартиал* , может иметь значение GUID \_ null для основного типа, подтипа или типа формата. Все элементы со \_ значениями NULL GUID не проверяются. (По сути, GUID \_ NULL выступает в качестве подстановочного знака.) Элементы со значениями, отличными от GUID \_ null, должны соответствовать типу носителя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




