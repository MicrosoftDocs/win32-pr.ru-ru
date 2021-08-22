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
ms.openlocfilehash: 5bd3462da5b8403f4db8f4727c0baa0a825e0db62b95216801300442d5cc393c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586274"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




