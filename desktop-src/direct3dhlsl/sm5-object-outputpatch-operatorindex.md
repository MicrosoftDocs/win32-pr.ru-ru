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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352712"
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

## <a name="remarks"></a>Примечания

Эта функция поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[аутпутпатч](sm5-object-outputpatch.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




