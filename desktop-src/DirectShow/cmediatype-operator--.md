---
description: Этот оператор проверяет равенство между объектами Кмедиатипе.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'Кмедиатипе. Кмедиатипе:: operator = = метод (Мтипе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93bc74338f994b967f313b7ed77529f9d90a8d01992b74cf4010f9aa51ab6a9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043654"
---
# <a name="cmediatypecmediatypeoperator-method"></a>Кмедиатипе. Кмедиатипе:: operator = = метод

Этот оператор проверяет равенство между объектами [**кмедиатипе**](cmediatype.md) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RT* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на объект **кмедиатипе** для сравнения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если *RT* равно этому объекту. В противном случае возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




