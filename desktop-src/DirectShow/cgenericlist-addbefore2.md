---
description: Метод Аддбефоре вставляет список перед указанной позицией. Этот метод использует параметры "POS" и "pList".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Кженериклист. Аддбефоре, метод (Вкслист. h) — параметры POS, pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821588"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a>Кженериклист. Аддбефоре, метод (Вкслист. h) — параметры POS, pList

`AddBefore`Метод вставляет список перед указанной позицией.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Расположение для вставки списка. Список вставляется перед этой позицией.

</dd> <dt>

*pList* 
</dt> <dd>

Указатель на список для вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха. В противном случае возвращает **значение false**.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




