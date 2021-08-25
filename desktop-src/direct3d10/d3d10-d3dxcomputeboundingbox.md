---
description: Функция D3DXComputeBoundingBox (D3DX10math. h) — вычисление ограничивающего прямоугольника, ориентированного на ось координат.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Функция D3DXComputeBoundingBox (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 30660e13dc726d9a1f5a1cd396b80298add58cc07d99bccd32709cba001311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028724"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a>Функция D3DXComputeBoundingBox (D3DX10math. h)

Вычисляются ориентированный ограничивающий прямоугольник на оси координат.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфирстпоситион* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Указатель на первую точку.

</dd> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число вершин.

</dd> <dt>

*двстриде* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Количество или число байтов между вершинами.

</dd> <dt>

*ПМИН* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий возвращенный нижний левый угол ограничивающего прямоугольника.

</dd> <dt>

*ПМАКС* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий возвращенный правый верхний угол ограничивающего прямоугольника.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
