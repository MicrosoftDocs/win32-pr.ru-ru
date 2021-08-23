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
ms.openlocfilehash: 41e821d853a8a8f981f1174d654f17475c0363cdcc97bb537e308ccd72e38190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987204"
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

## <a name="remarks"></a>Remarks

После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования. Этот метод определяет, какие исправления являются смежными (в пределах указанного допуска). Эта информация используется внутренним образом для оптимизации тесселяции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: OPTIMIZE**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
