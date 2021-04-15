---
description: Метод Финди извлекает первую позицию, содержащую указанный элемент.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Кбаселист. Финди, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668608"
---
# <a name="cbaselistfindi-method"></a>Кбаселист. Финди, метод

`FindI`Метод извлекает первую позицию, содержащую указанный элемент.

## <a name="syntax"></a>Синтаксис


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побж* 
</dt> <dd>

Указатель на элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение позиции или **значение NULL** , если элемент отсутствует в списке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




