---
description: Метод Аддафтер вставляет элемент после указанной позиции и использует параметры "p" и "Побж".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Кженериклист. Аддафтер, метод (Вкслист. h) — p, параметры Побж
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356153"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a>Кженериклист. Аддафтер, метод (Вкслист. h) — p, параметры Побж

`AddAfter`Метод вставляет элемент после указанной позиции.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Позиция, после которой нужно добавить элемент. Если значение *p* равно **null**, метод добавляет элемент в заголовок списка.

</dd> <dt>

*побж* 
</dt> <dd>

Указатель на объект типа **Object** (тип шаблона).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индикатор позиции вставленного элемента.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




