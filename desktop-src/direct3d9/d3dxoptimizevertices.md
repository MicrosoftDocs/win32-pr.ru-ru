---
description: Создает оптимизированное повторное сопоставление вершин для списка треугольников. Эта функция обычно используется после применения повторного сопоставления лица, созданного с помощью D3DXOptimizeFaces.
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: Функция D3DXOptimizeVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 734c2224ae29e7ab166010d59859d00355e5400e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720865"
---
# <a name="d3dxoptimizevertices-function"></a>Функция D3DXOptimizeVertices

Создает оптимизированное повторное сопоставление вершин для списка треугольников. Эта функция обычно используется после применения повторного сопоставления лица, созданного с помощью [**D3DXOptimizeFaces**](d3dxoptimizefaces.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
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

Число сторон в списке треугольников.

</dd> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число вершин, на которые ссылается список треугольников.

</dd> <dt>

*Indices32Bit* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Флаг, указывающий тип индекса: **true** , если индексы являются 32-разрядными (более 65535 вершинами), **значение false** , если индексы являются 16-разрядными (65535 или меньше вершин).

</dd> <dt>

*пвертексремап* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на целевой буфер, который будет содержать новый индекс для каждой вершины. Значение, хранящееся в *пвертексремап* для данного элемента, является расположением исходной вершины в новом упорядочении вершин.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

По умолчанию при создании сетка использует 16 битовых индексов, если в приложении не указано иное. Чтобы проверить, использует ли существующая сетка 16-разрядные или 32-битовые индексы, вызовите [**ID3DXBaseMesh::-Options**](id3dxbasemesh--getoptions.md) и проверьте флаг D3DXMESH-bit \_ .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
