---
description: Функция D3DXComputeBoundingBox (D3DX9Mesh. h) — вычисление ограничивающего прямоугольника, ориентированного на ось координат.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Функция D3DXComputeBoundingBox (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03eb722e68b58ec48a3bf607ab72d67004ad30a0c765b19c1b84ae29577c773b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299956"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>Функция D3DXComputeBoundingBox (D3DX9Mesh. h)

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

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

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

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий возвращенный нижний левый угол ограничивающего прямоугольника. См. заметки.

</dd> <dt>

*ПМАКС* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий возвращенный правый верхний угол ограничивающего прямоугольника. См. заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
