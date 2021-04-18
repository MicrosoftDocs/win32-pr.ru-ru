---
description: Выполняет вычисление векторов касательных координат текстуры, заданных на стадии текстуры. Предоставляется для поддержки устаревших приложений. Используйте D3DXComputeTangentFrameEx для улучшения результатов.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Функция D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713651"
---
# <a name="d3dxcomputetangent-function"></a>Функция D3DXComputeTangent

Выполняет вычисление векторов касательных координат текстуры, заданных на стадии текстуры. Предоставляется для поддержки устаревших приложений. Используйте [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) для улучшения результатов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Сетка* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , который представляет входную сетку.

</dd> <dt>

*Тексстажеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс, представляющий этап текстуры.

</dd> <dt>

*Танжентиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс, предоставляющий индекс использования для данных касательно. Объявление вершины подразумевает использование; Этот индекс изменяет использование с помощью индекса использования. Дополнительные сведения об объявлении вершин см. в разделе [объявление вершины (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*Бинорминдекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс, предоставляющий индекс использования для данных бинормал. Объявление вершины подразумевает использование; Этот индекс изменяет использование с помощью индекса использования. Дополнительные сведения об объявлении вершин см. в разделе [объявление вершины (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*Перенос по словам* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Присвойте этому параметру значение 0, чтобы не выполнять перенос, или значение 1 для переноса в нужные и V направлениях.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который должен быть заполнен смежными индексами граней. Число байтов в этом массиве должно быть не меньше ((3 \* [**жетнумфацес**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Если в объявлении вершины сетки заданы поля тангенса или бинормал, **D3DXComputeTangent** будет обновлять любые данные о тангенсе или бинормал данных, предоставляемые пользователем. Кроме того, задайте для Танжентиндекс значение [D3DX \_ по умолчанию](other-d3dx-constants.md) , чтобы не обновлять предоставляемые пользователем данные касательно, или задайте для бинорминдекс значение D3DX \_ по умолчанию, чтобы не обновлять данные бинормал, предоставляемые пользователем. Тексстажеиндекс не может иметь значение D3DX \_ по умолчанию.

**D3DXComputeTangent** зависит от объявления вершины сетки, содержащего либо поле Бинормал (бинорминдекс), либо поле тангенса (танжентиндекс), либо и то, и другое. Если оба этих флажка отсутствуют, эта функция завершится ошибкой.

Эта функция просто вызывает [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) со следующими входными параметрами:


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
