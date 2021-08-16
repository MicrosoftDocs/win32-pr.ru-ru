---
description: Создает оптимизированное сопоставление лиц для списка треугольников.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Функция D3DXOptimizeFaces (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 165f81d9b829ce7a7b22ced6fb37851f926ed861f11b79feca3a63c763dabbb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525233"
---
# <a name="d3dxoptimizefaces-function"></a>Функция D3DXOptimizeFaces

Создает оптимизированное сопоставление лиц для списка треугольников.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пиндицес* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на индексы списка треугольников для использования при упорядочивании вершин.

</dd> <dt>

*Нумфацес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число сторон в списке треугольников. Для 16-разрядных сеток это ограничение составляет 2 ^ 16-1 (65535) или меньше лиц.

</dd> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число вершин, на которые ссылается список треугольников.

</dd> <dt>

*Indices32Bit* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Флаг, указывающий тип индекса: **true** , если индексы являются 32-разрядными (более 65535 индексами), **значение false** , если индексы являются 16-разрядными (65535 или меньшего количества индексов).

</dd> <dt>

*пфацеремап* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на исходную сетчатую линию, разделенную для создания текущего лица.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Процедура оптимизации этой функции функционально эквивалентна вызову [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) с \_ флагом D3DXMESHOPT девицеиндепендент, но эта функция делает более эффективное использование кэшей вершин.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
