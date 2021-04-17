---
description: Этот оператор проверяет, что одно время ссылки меньше или равно другому.
ms.assetid: ae7449b7-d319-4e76-892f-0f9ae63ddf94
title: Коарефтиме. operator>= метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator>=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69b345f42c854e939c21a028827889a03e0ce735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675851"
---
# <a name="coareftimeoperator-method"></a>Коарефтиме. operator>= метод

Этот оператор проверяет, что одно время ссылки меньше или равно другому.

## <a name="syntax"></a>Синтаксис


```C++
BOOL operator>=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RT* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на объект **коарефтиме** для сравнения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если этот объект меньше или равен *RT*. В противном случае возвращает **значение false**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Коарефтиме**](coareftime.md)
</dt> </dl>

 

 




