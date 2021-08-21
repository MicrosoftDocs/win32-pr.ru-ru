---
description: Метод Аддхеад добавляет список в начало списка.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Кженериклист. Аддхеад, метод (Вкслист. h) — параметр pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c26667ce12af902f3d5cf355a6556dc95e5dd1f5e0cad77f944e663eeef8ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656150"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a>Кженериклист. Аддхеад, метод (Вкслист. h) — параметр pList

`AddHead`Метод добавляет список в начало списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pList* 
</dt> <dd>

Указатель на список элементов для добавления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Заголовок | вкслист. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




