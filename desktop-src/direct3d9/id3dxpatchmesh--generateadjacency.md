---
description: Создание списка границ сетки и исправлений, которые совместно используют каждое ребро.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'Метод ID3DXPatchMesh:: Женератеаджаценци (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424334"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>Метод ID3DXPatchMesh:: Женератеаджаценци

Создание списка границ сетки и исправлений, которые совместно используют каждое ребро.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фтолеранце* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Указывает, что вершины, которые отличаются в положении на меньшее допустимое отклонение, должны рассматриваться как коинЦидент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования. Этот метод определяет, какие исправления являются смежными (в пределах указанного допуска). Эта информация используется внутренним образом для оптимизации тесселяции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: OPTIMIZE**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
