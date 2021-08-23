---
description: Функция D3DXComputeBoundingSphere (D3DX9Mesh. h) — вычисление ограничивающей сферы для сетки.
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Функция D3DXComputeBoundingSphere (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0eee5def85163e75f90a8eeb6a063876e19c49b4997abb38d387a2f05c0a8fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857424"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a>Функция D3DXComputeBoundingSphere (D3DX9Mesh. h)

Вычисление ограничивающей сферы для сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
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

Число байтов между векторами позиционирования. Чтобы получить шаг вершин, используйте [**жетнумбитеспервертекс**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)или [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) .

</dd> <dt>

*пцентер* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Структура [**D3DXVECTOR3**](d3dxvector3.md) , определяющая центр координат возвращаемой ограничивающей сферы.

</dd> <dt>

*Прадиус* \[ заполняет\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Радиус возвращаемой ограничивающей сферы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
