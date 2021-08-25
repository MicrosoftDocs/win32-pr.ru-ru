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
ms.openlocfilehash: 6de0037d76e63049294b0455c8ec1fbac82963d94febb35f7c9400ec8eae9ab5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697534"
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

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Заголовок | вкслист. h (включает Потоки. h) |
| Библиотека| Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




