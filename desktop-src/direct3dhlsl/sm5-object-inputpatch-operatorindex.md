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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273482"
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

## <a name="remarks"></a>Примечания

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

 

 




