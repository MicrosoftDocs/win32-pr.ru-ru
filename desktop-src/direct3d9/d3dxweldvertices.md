---
description: Расшов объединяет реплицированные вершины с одинаковыми атрибутами. Этот метод использует указанные значения Эпсилон для сравнения на равенство.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Функция D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6a9a05573467e0725785a6272e5542c4f871080fe221ac12078b17165eb5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803277"
---
# <a name="d3dxweldvertices-function"></a>Функция D3DXWeldVertices

Расшов объединяет реплицированные вершины с одинаковыми атрибутами. Этот метод использует указанные значения Эпсилон для сравнения на равенство.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на объект [**ID3DXMesh**](id3dxmesh.md) — сетку, из которой следует расшов вершины.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов из [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*пепсилонс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Указатель на структуру [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , в которой указываются значения Эпсилон, используемые для этого метода. Используйте **значение NULL** , чтобы инициализировать все члены структуры до значения по умолчанию 1.0 e-6f.

</dd> <dt>

*паджаценциин* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в исходной сетке. Если у границы нет смежных сторон, значение равно 0xFFFFFFFF. Если этот параметр имеет значение **null**, будет вызван [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md) для создания логической информации о соседства.

</dd> <dt>

*паджаценциаут* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в оптимизированной сетке. Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.

</dd> <dt>

*пфацеремап* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Массив DWORD, по одному на каждый из них, который определяет исходную сетку, соответствующую каждой грани в раскадровой сетке.

</dd> <dt>

*ппвертексремап* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами. Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Эта функция использует предоставляемые сведения о смежности для определения реплицируемых точек. Вершины сливаются на основе сравнения Эпсилон. Вершины с равным положением уже должны быть вычислены и представлены данными-представителями.

Эта функция сочетает в себе логически разпепсилонс вершины, имеющие аналогичные компоненты, такие как нормали или координаты текстуры в.

В следующем примере кода вызывается эта функция с включенным Велдинг. Вершины сравниваются с использованием значений Эпсилон для обычных векторов и позиций вершин. Указатель возвращается в массив пересопоставления лицевой стороны (*пфацеремап*).


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
