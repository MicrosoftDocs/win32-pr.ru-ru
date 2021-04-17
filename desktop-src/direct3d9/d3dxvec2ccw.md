---
description: Возвращает компонент z, используя перекрестное произведение двух двумерных векторов.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Функция D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703767"
---
# <a name="d3dxvec2ccw-function"></a>Функция D3DXVec2CCW

Возвращает компонент z, используя перекрестное произведение двух двумерных векторов.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pV1* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> <dt>

*pV2* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Компонент z.

## <a name="remarks"></a>Комментарии

Эта функция определяет компонент z, определяя перекрестные произведения на основе следующей формулы: ((x1, y1, 0) Cross (x2, Y2, 0)). Или, как показано в следующем примере.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Если значение z-компонента положительное, вектор v2 имеет против часовой стрелки от вектора v1. Эти сведения полезны для отбора обратной стороны.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
