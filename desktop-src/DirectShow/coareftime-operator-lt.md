---
description: Этот оператор проверяет, меньше ли одно время ссылки, чем другое.
ms.assetid: 709fb861-a836-4a20-8c93-c0e8ab79f377
title: Метод< Коарефтиме. operator (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator<
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d98c80e33cebabb868785d1df4d78ca038963683af5d778386ba0d85432e0e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073838"
---
# <a name="coareftimeoperator-method"></a>Коарефтиме. operator< метод

Этот оператор проверяет, меньше ли одно время ссылки, чем другое.

## <a name="syntax"></a>Синтаксис


```C++
BOOL operator<(
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

Возвращает **значение true** , если этот объект строго меньше *RT*. В противном случае возвращает **значение false**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Коарефтиме**](coareftime.md)
</dt> </dl>

 

 




