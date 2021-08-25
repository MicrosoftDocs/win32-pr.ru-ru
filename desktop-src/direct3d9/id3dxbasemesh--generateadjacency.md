---
description: 'Метод ID3DXBaseMesh:: Женератеаджаценци — создает список границ сетки, а также список лиц, совместно использующих каждое ребро.'
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'Метод ID3DXBaseMesh:: Женератеаджаценци (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d51070b5b67b50859338943a60e44cbb224e572ab9e5704e56940328a65479f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848534"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>Метод ID3DXBaseMesh:: Женератеаджаценци

Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Эпсилон* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Указывает, что вершины, отличающиеся от позиций меньше Эпсилон, должны рассматриваться как коинЦидент.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на массив из трех DWORD на грань, который должен быть заполнен индексами смежных граней. Число байтов в этом массиве должно быть не менее 3 \* [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

После того как приложение создаст сведения о смежности для сетки, данные сетки можно оптимизировать для повышения производительности рисования.

Порядок записей в смежном буфере определяется порядком индексов вершин в буфере индекса. Смежный треугольник 0 всегда соответствует границе между индексами углов 0 и 1. Смежный треугольник 1 всегда соответствует границе между индексами углов 1 и 2, а смежный треугольник 2 соответствует границе между индексами углов 2 и 0.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh:: OPTIMIZE**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh:: Оптимизеинплаце**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
