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
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105665015"
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
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




