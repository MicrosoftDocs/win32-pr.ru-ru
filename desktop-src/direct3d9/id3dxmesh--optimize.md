---
description: 'Метод ID3DXMesh:: optimize — создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.'
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Метод ID3DXMesh:: optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4ea03bcaaab492ec09dd24ec93c6a9c9ca393c1399b05e12096a8ba1f4f9aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493104"
---
# <a name="id3dxmeshoptimize-method"></a>Метод ID3DXMesh:: OPTIMIZE

Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Указывает тип выполняемой оптимизации. Этому параметру можно присвоить сочетание из одного или нескольких флагов из [**D3DXMESHOPT**](./d3dxmeshopt.md) и [**D3DXMESH**](./d3dxmesh.md) (за исключением D3DXMESH \_ 32-разрядной версии, D3DXMESH с помощью \_ \_ WriteOnly и D3DXMESH \_ WRITEONLY).

</dd> <dt>

*паджаценциин* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, указывающий три соседа для каждой грани в исходной сетке. Если у границы нет смежных сторон, значение равно 0xFFFFFFFF. См. заметки.

</dd> <dt>

*паджаценциаут* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на массив из трех DWORD на грань, указывающий три соседа для каждой грани в оптимизированной сетке. Если у границы нет смежных сторон, значение равно 0xFFFFFFFF.

</dd> <dt>

*пфацеремап* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Массив DWORD, по одному на каждый из них, который определяет исходную сетку, соответствующую каждой грани в оптимизированной сетке. Если значение, заданное для этого аргумента, равно **null**, данные сопоставления лиц не возвращаются.

</dd> <dt>

*ппвертексремап* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , который содержит DWORD для каждой вершины, указывающий, как новые вершины сопоставляются со старыми вершинами. Такое перераспределение полезно, если необходимо изменить внешние данные на основе нового сопоставления вершин.

</dd> <dt>

*ппоптмеш* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий оптимизированную сетку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Этот метод создает новую сетку. Перед запуском optimize приложение должно создать буфер соседей путем вызова [**ID3DXBaseMesh:: женератеаджаценци**](id3dxbasemesh--generateadjacency.md). В буфере соседка содержатся смежные данные, например список краев и сторон, расположенных рядом друг с другом.

Этот метод очень похож на метод [**ID3DXBaseMesh:: клонемеш**](id3dxbasemesh--clonemesh.md) , за исключением того, что он может выполнять оптимизацию при формировании нового клона сетки. Выходная сетка наследует все параметры создания входной сетки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: Оптимизеинплаце**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
