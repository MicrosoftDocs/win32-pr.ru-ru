---
description: Метод конструктора Кбаселист. Кбаселист.
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Конструктор Кбаселист. Кбаселист (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b734722371aa80e3c120dde3c6fb629785dfc6cdf9786c7f4ab1cbea87e5559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016982"
---
# <a name="cbaselistcbaselist-constructor"></a>Кбаселист. Кбаселист, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя списка.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для повышения эффективности `CBaseList` класс поддерживает кэш узлов списка. Эта версия конструктора использует размер кэша по умолчанию.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




