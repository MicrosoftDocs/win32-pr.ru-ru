---
description: Возвращает размер исправления треугольника.
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: Функция D3DXTriPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 54eba8131d59b9d1e68526cd26bb74b497bcec21fcbffdb4229678f166646806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298246"
---
# <a name="d3dxtripatchsize-function"></a>Функция D3DXTriPatchSize

Возвращает размер исправления треугольника.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфнумсегс* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Число сегментов на границе для тесселяции.

</dd> <dt>

*пдвтрианглес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на DWORD, содержащий число треугольников в исправлении.

</dd> <dt>

*пдввертицес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на DWORD, содержащий число вершин в исправлении треугольника.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
