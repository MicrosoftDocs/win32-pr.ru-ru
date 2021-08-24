---
description: Формирует упрощенную сетку, используя указанные весовые коэффициенты, которые максимально близко к данному MinValue.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Функция D3DXSimplifyMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cc0bfe18afef7b91dbdf887500b485a446b154cb5775cbf950a7e712a332a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749784"
---
# <a name="d3dxsimplifymesh-function"></a>Функция D3DXSimplifyMesh

Формирует упрощенную сетку, используя указанные весовые коэффициенты, которые максимально близко к данному MinValue.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий исходную сетку.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сетке, которую необходимо упростить.

</dd> <dt>

*пвертексаттрибутевеигхтс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

Указатель на структуру [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , содержащую вес для каждого компонента вершины. Если этот параметр имеет значение **null**, используется структура по умолчанию. См. заметки.

</dd> <dt>

*пвертексвеигхтс* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на массив весовых коэффициентов вершин. Если этот параметр имеет значение **null**, все веса вершин имеют значение 1,0.

</dd> <dt>

*MinValue* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Количество вершин или граней в зависимости от флага, установленного в параметре *Options* , с помощью которого можно упростить исходную сетку.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Задает параметры упрощения для сетки. Можно задать один из флагов в [**D3DXMESHSIMP**](./d3dxmeshsimp.md) .

</dd> <dt>

*ппмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий возвращенную сетку упрощения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Эта функция создает сетку, которая содержит вершины или грани *MinValue* .

Если процесс упрощения не может сократить сетку до *MinValue*, вызов по-прежнему будет выполнен, так как значение *MinValue* является желаемым минимумом, а не абсолютным минимумом.

Если *пвертексаттрибутевеигхтс* имеет значение **null**, то структуре [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) по умолчанию присваиваются следующие значения.


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



Эта структура по умолчанию используется большинством приложений, так как она учитывает только геометрическую и нормальную корректировку. В особых случаях необходимо изменить другие поля элементов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
