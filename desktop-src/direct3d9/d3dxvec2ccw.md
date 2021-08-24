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
ms.openlocfilehash: 2b38adaf28b6e2394608cfb6f73f4a39d803d4fd5106f826d810a5c8dfd02618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630704"
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

## <a name="remarks"></a>Remarks

Эта функция определяет компонент z, определяя перекрестные произведения на основе следующей формулы: ((x1, y1, 0) Cross (x2, Y2, 0)). Или, как показано в следующем примере.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Если значение z-компонента положительное, вектор v2 имеет против часовой стрелки от вектора v1. Эти сведения полезны для отбора обратной стороны.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
