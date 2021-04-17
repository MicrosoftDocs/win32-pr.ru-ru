---
description: Выполняет однородную тесселяцию на основе уровня тесселяции.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'Метод ID3DXPatchMesh:: тесселяции (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105665004"
---
# <a name="id3dxpatchmeshtessellate-method"></a>Метод ID3DXPatchMesh:: тесселяции

Выполняет однородную тесселяцию на основе уровня тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фтесслевел* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Уровень тесселяции. Это число вершин, появившихся между существующими вершинами. Диапазон этого параметра с плавающей запятой равен 0 < Фтесслевел <= 32.

</dd> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Результирующая Тесселяция сетки. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Эта функция будет работать более эффективно, если сетка исправлений оптимизирована с помощью [**ID3DXPatchMesh:: optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
