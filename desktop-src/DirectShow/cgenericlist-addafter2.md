---
description: Метод Аддафтер вставляет список после указанной должности и использует параметры "POS" и "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Кженериклист. Аддафтер, метод (Вкслист. h) — параметры POS, plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 846e37b961af8d2492b3aff032193e87fb3603eb1751c25f0e3ca8e0c5d38618
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697484"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a>Кженериклист. Аддафтер, метод (Вкслист. h) — параметры POS, plist

`AddAfter`Метод вставляет список после указанной позицией.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Расположение для вставки списка. Список вставляется после этой должности.

</dd> <dt>

*pList* 
</dt> <dd>

Указатель на список для вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Заголовок | вкслист. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




