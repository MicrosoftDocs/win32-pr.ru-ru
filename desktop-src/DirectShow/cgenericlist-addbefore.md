---
description: Метод Аддбефоре вставляет элемент перед указанной позицией. Этот метод использует параметры "p" и "Побж".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Кженериклист. Аддбефоре, метод (Вкслист. h) — p, параметры Побж
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000546"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a>Кженериклист. Аддбефоре, метод (Вкслист. h) — p, параметры Побж

`AddBefore`Метод вставляет элемент перед указанной позицией.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ш* 
</dt> <dd>

Расположение, до которого необходимо вставить список. Если значение *p* равно **null**, этот метод добавляет элемент в конец списка.

</dd> <dt>

*побж* 
</dt> <dd>

Указатель на объект типа **Object** (тип шаблона).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индикатор позиции для вставленного элемента.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Header | Вкслист. h (включение Streams. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




