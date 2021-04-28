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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096331"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




