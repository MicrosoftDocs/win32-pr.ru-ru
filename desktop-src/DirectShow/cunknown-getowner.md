---
description: Метод DataGridViewCell получает указатель на интерфейс IUnknown компонента-владельца. Для агрегированного компонента владельцем является внешний компонент. В противном случае компонент владеет самим собой.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Метод Кункновн. метод Owner (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657781"
---
# <a name="cunknowngetowner-method"></a>Кункновн. метод Owner

`GetOwner`Метод получает указатель на интерфейс **IUnknown** компонента-владельца. Для агрегированного компонента владельцем является внешний компонент. В противном случае компонент владеет самим собой.

## <a name="syntax"></a>Синтаксис


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на управляющий интерфейс **IUnknown** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




