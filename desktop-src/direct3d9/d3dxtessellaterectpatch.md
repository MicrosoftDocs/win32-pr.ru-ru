---
description: Разбивает прямоугольное исправление поверхности более высокого порядка в сетку с треугольником.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Функция D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273757"
---
# <a name="d3dxtessellaterectpatch-function"></a>Функция D3DXTessellateRectPatch

Разбивает прямоугольное исправление поверхности более высокого порядка в сетку с треугольником.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ПВБ* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Буфер вершин, содержащий данные исправления.

</dd> <dt>

*пнумсегс* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на массив из четырех значений с плавающей запятой, определяющих количество сегментов, на которые должны быть разбиты все границы данного обновления прямоугольника при тесселяции. См [**. \_ сведения о D3DRECTPATCH**](d3drectpatch-info.md).

</dd> <dt>

*пиндекл* \[ окне\]
</dt> <dd>

Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Структура объявления вершин, определяющая данные вершин. См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*пректпатчинфо* \[ окне\]
</dt> <dd>

Тип: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***

Описывает прямоугольное исправление. См [**. \_ сведения о D3DRECTPATCH**](d3drectpatch-info.md).

</dd> <dt>

*пмеш* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на созданную сетку. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Используйте [**D3DXRectPatchSize**](d3dxrectpatchsize.md) , чтобы получить количество выходных вершин и индексов, необходимых для функции тесселяции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
