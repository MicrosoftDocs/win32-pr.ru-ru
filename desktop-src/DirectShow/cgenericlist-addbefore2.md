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
ms.openlocfilehash: 6f05d67477bb7e6c89eddfe0a68ad47d83760762fc68cddf6f73c731886f88d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697454"
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

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Заголовок | вкслист. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




