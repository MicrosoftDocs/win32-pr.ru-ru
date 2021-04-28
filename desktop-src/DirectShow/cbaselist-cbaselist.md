---
description: Метод конструктора Кбаселист. Кбаселист (TCHAR \* , int).
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Конструктор Кбаселист. Кбаселист (TCHAR *, INT) (Вкслист. h)
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099642"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a>Конструктор Кбаселист. Кбаселист (TCHAR \* , int)

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на имя списка.

</dd> <dt>

*иитемс* 
</dt> <dd>

Размер кэша узлов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Для повышения эффективности `CBaseList` класс поддерживает кэш узлов списка. Если вы понимаете, сколько элементов будет храниться в списке, используйте эту версию конструктора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




