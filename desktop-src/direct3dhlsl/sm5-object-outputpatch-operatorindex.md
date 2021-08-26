---
title: 'Функция Аутпутпатч:: operator'
description: 'Возвращает значение n точки управления в исправлении. | Функция Аутпутпатч:: operator'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 684925491ce7b5ac50cb293b3c8a0270557c9b9e65fcfcde63e9699127bc7ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023474"
---
# <a name="outputpatchoperator--function"></a>Функция Аутпутпатч:: operator

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
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[аутпутпатч](sm5-object-outputpatch.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




