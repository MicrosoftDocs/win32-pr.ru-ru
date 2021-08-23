---
description: Задает значение влияния кости на одну вершину.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'Метод ID3DXSkinInfo:: Сетбоневертексинфлуенце (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 950c72ed89c9204fb2369f175effd381548cb1913e9a2949666f6a0f4ea9aad9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674694"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a>Метод ID3DXSkinInfo:: Сетбоневертексинфлуенце

Задает значение влияния кости на одну вершину.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*боненум* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс кости. Значение должно находиться в диапазоне от 0 до количества костей.

</dd> <dt>

*инфлуенценум* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс массива влияния указанной кости.

</dd> <dt>

*вес* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Влияние коэффициента смешения на указанную кость.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Жетбоневертексинфлуенце**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс**](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[**ID3DXSkinInfo:: Жетбонеинфлуенце**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
