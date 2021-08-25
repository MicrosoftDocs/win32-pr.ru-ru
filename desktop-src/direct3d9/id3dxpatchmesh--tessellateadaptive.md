---
description: Выполняет адаптивную тесселяцию на основе z-критерия адаптивной тесселяции.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'Метод ID3DXPatchMesh:: Тесселлатеадаптиве (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6365cfcf50debfeeb28fd493b76ac60943ee14f27a2dadec168b3dd4d31ace1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856294"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>Метод ID3DXPatchMesh:: Тесселлатеадаптиве

Выполняет адаптивную тесселяцию на основе z-критерия адаптивной тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птранс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Задает вектор 4D, который имеет пунктирные вершины для получения суммы адаптивной тесселяции для каждого вершины. Каждый ребр размещается в среднем значении уровней тесселяции для двух вершин, к которым он подключается.

</dd> <dt>

*двмакстесслевел* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Максимальный предел адаптивной тесселяции. Это число вершин, появившихся между существующими вершинами. Это целое значение может находиться в диапазоне от 1 до 32 включительно.

</dd> <dt>

*двминтесслевел* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Минимальный предел для адаптивной тесселяции. Это число вершин, появившихся между существующими вершинами. Это целое значение может находиться в диапазоне от 1 до 32 включительно.

</dd> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Результирующая Тесселяция сетки. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Эта функция будет работать более эффективно, если сетка исправлений оптимизирована с помощью [**ID3DXPatchMesh:: optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
