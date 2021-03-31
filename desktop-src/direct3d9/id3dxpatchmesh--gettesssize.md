---
description: Возвращает размер тесселяции сетки по заданному уровню тесселяции.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'Метод ID3DXPatchMesh:: Жеттесссизе (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef23f46baca7e05005cee83f6ca765b9a5214b8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081952"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>Метод ID3DXPatchMesh:: Жеттесссизе

Возвращает размер тесселяции сетки по заданному уровню тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фтесслевел* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Уровень тесселяции.

</dd> <dt>

*Адаптивное* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Адаптивное тесселяция. Для адаптивной тесселяции присвойте этому параметру значение **true** и задайте для фтесслевел максимальное значение тесселяции. Это приведет к максимальному размеру сетки, необходимой для адаптивной тесселяции.

</dd> <dt>

*Нумтрианглес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на число треугольников, создаваемых тесселяцией сетки.

</dd> <dt>

*Нумвертицес* \[ заполняет\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на число вершин, созданных мозаикой сетки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Этот метод предполагает однородную тесселяцию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
