---
description: Тесселяция треугольного исправления поверхности с более высоким порядком в сетке с треугольником.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Функция D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1cae3ff9709cb74e15c176abc0e738e4f12d1417eec1d040b90269b7e3cbc6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122716"
---
# <a name="d3dxtessellatetripatch-function"></a>Функция D3DXTessellateTriPatch

Тесселяция треугольного исправления поверхности с более высоким порядком в сетке с треугольником.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
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

Указатель на массив из трех значений с плавающей запятой, определяющих количество сегментов, на которые должно быть разбито каждое из них. См [**. \_ сведения о D3DTRIPATCH**](d3dtripatch-info.md).

</dd> <dt>

*пиндекл* \[ окне\]
</dt> <dd>

Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Структура объявления вершин, определяющая данные вершин. См. [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*птрипатчинфо* \[ окне\]
</dt> <dd>

Тип: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***

Описывает исправление треугольника. См [**. \_ сведения о D3DTRIPATCH**](d3dtripatch-info.md).

</dd> <dt>

*пмеш* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на созданную сетку. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Используйте [**D3DXTriPatchSize**](d3dxtripatchsize.md) , чтобы получить количество выходных вершин и индексов, необходимых для функции тесселяции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
