---
description: Метод AddTail добавляет список в конец списка.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Кженериклист. AddTail, метод (Вкслист. h) — параметр pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105656827"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a>Кженериклист. AddTail, метод (Вкслист. h) — параметр pList

`AddTail`Метод добавляет список в конец списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pList* 
</dt> <dd>

Указатель на добавляемый список.

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

 

 




