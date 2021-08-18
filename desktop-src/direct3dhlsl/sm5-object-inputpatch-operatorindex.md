---
title: 'Функция Инпутпатч:: operator'
description: 'Возвращает значение n точки управления в исправлении. | Функция Инпутпатч:: operator'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- Оператор Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81c768d138f6ee1853f9930a56f1a1864b468e8be9ff421f4dba1698b790053c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986034"
---
# <a name="inputpatchoperator--function"></a>Функция Инпутпатч:: operator

Возвращает *n*-<sup>е</sup> контрольную точку в исправлении.

## <a name="syntax"></a>Синтаксис

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*n* \[ в\]
</dt> <dd>

Тип: **uint**

Входной индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **T**

*N*-<sup>я</sup> контрольная точка.

## <a name="remarks"></a>Remarks

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[инпутпатч](sm5-object-inputpatch.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




