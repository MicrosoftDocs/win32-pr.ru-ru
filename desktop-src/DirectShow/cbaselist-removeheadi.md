---
description: Метод Ремовехеади удаляет первый элемент из списка.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Кбаселист. Ремовехеади, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668897"
---
# <a name="cbaselistremoveheadi-method"></a>Кбаселист. Ремовехеади, метод

`RemoveHeadI`Метод удаляет первый элемент из списка.

## <a name="syntax"></a>Синтаксис


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на элемент или **значение NULL** , если список пуст.

## <a name="remarks"></a>Комментарии

Этот метод удаляет узел списка, но не элемент, содержащийся в узле.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




