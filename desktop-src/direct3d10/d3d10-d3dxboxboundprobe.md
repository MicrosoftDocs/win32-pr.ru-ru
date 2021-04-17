---
description: Функция D3DXBoxBoundProbe (D3DX10math. h) определяет, пересекает ли луч том ограничивающего прямоугольника бокса.
ms.assetid: d3cdcf89-461b-44b0-b5d0-ca2e3869a5ad
title: Функция D3DXBoxBoundProbe (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e1a8d1a7b879814cff43e31b060cc2af53167818
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187817"
---
# <a name="d3dxboxboundprobe-function-d3dx10mathh"></a>Функция D3DXBoxBoundProbe (D3DX10math. h)

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

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), описывающий левый нижний угол ограничивающего прямоугольника. См. заметки.

</dd> <dt>

*ПМАКС* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий правый верхний угол ограничивающего прямоугольника. См. заметки.

</dd> <dt>

*прайпоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3, задавая координату начала луча.

</dd> <dt>

*прайдиректион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на структуру D3DXVECTOR3, в которой указывается направление луча. Этот вектор не должен быть (0, 0, 0), но не требует нормализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если луч пересекает том ограничивающего прямоугольника бокса. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

**D3DXBoxBoundProbe** определяет, пересекает ли луч том ограничивающего прямоугольника бокса, а не только поверхность бокса.

Значения, передаваемые в **D3DXBoxBoundProbe** , — это xMin, xMax, yMin, yMax, змин и змакс. Таким же ниже определяются углы ограничивающего прямоугольника.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок  | D3DX10math. h |
| Библиотека | D3DX10. lib  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
