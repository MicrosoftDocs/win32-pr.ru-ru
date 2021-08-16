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
ms.openlocfilehash: c741a6820d414d7a00ad0a9fef768d982f2335c9cb9d8417e42376ea243cc58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076044"
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
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




