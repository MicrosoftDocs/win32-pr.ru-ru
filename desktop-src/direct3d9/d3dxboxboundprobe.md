---
description: Определяет, пересекает ли луч том ограничивающего прямоугольника бокса.
ms.assetid: 45ff8540-ed5c-4f54-b3b7-3385087a6863
title: Функция D3DXBoxBoundProbe (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBoxBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 197582c2f404124edd5a49c9d7780ce35cac61b15438a81d120839f283b82373
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676394"
---
# <a name="d3dxboxboundprobe-function"></a>Функция D3DXBoxBoundProbe

Определяет, пересекает ли луч том ограничивающего прямоугольника бокса.

## <a name="syntax"></a>Синтаксис


```C++
BOOL D3DXBoxBoundProbe(
  _In_ const D3DXVECTOR3 *pMin,
  _In_ const D3DXVECTOR3 *pMax,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПМИН* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий левый нижний угол ограничивающего прямоугольника. См. заметки.

</dd> <dt>

*ПМАКС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий правый верхний угол ограничивающего прямоугольника. См. заметки.

</dd> <dt>

*прайпоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , задавая координату начала луча.

</dd> <dt>

*прайдиректион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается направление луча. Этот вектор не должен быть (0, 0, 0), но не требует нормализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если луч пересекает том ограничивающего прямоугольника бокса. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

**D3DXboxBoundProbe** определяет, пересекает ли луч том ограничивающего прямоугольника бокса, а не только поверхность бокса.

Значения, передаваемые в **D3DXboxBoundProbe** , — это xMin, xMax, yMin, yMax, змин и змакс. Таким же ниже определяются углы ограничивающего прямоугольника.


```
xmax, ymax, zmax
xmax, ymax, zmin
xmax, ymin, zmax
xmax, ymin, zmin
xmin, ymax, zmax
xmin, ymax, zmin
xmin, ymin, zmax
xmin, ymin, zmin
```



Глубина ограничивающего прямоугольника в направлении по оси z равна змакс-змин, в направлении по оси y — ymax-ymin, а в направлении x — xmax-xmin. Например, при использовании следующих минимальных и максимальных векторов, min (-1,-1,-1) и Max (1, 1, 1) ограничивающий прямоугольник определяется следующим образом.


```
 1,  1,  1
 1,  1, -1
 1, -1,  1
 1, -1, -1
-1,  1,  1
-1,  1, -1
-1, -1,  1
-1, -1, -l
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeBoundingBox**](d3dxcomputeboundingbox.md)
</dt> </dl>

 

 
