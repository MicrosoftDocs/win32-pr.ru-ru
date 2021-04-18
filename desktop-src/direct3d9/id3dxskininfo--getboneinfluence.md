---
description: Возвращает вершины и весовые коэффициенты, влияющие на кость.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'Метод ID3DXSkinInfo:: Жетбонеинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713451"
---
# <a name="id3dxskininfogetboneinfluence-method"></a>Метод ID3DXSkinInfo:: Жетбонеинфлуенце

Возвращает вершины и весовые коэффициенты, влияющие на кость.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кость* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Номер кости.

</dd> <dt>

*вершины* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Получение массива вершин, на которые влияет кость.

</dd> <dt>

*весовые коэффициенты* \[ в, out\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Получение массива весов, на которые влияет кость.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Используйте [**ID3DXSkinInfo:: жетнумбонеинфлуенцес**](id3dxskininfo--getnumboneinfluences.md) , чтобы узнать, сколько вершин влияет на кость.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетбонеинфлуенце**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
