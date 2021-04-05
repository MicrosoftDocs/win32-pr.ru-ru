---
description: Метод Аддхеад добавляет элемент в начало списка.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Кженериклист. Аддхеад, метод (Вкслист. h) — параметр Побж
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
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104081962"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a>Кженериклист. Аддхеад, метод (Вкслист. h) — параметр Побж

`AddHead`Метод добавляет элемент в начало списка.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побж* 
</dt> <dd>

Указатель на объект типа **Object** (тип шаблона).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение расположения, указывающее новую головную точку. Если метод завершается ошибкой, возвращается значение **null**.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




