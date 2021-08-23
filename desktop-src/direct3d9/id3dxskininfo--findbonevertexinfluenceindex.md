---
description: Извлекает индекс кости, влияющей на одну вершину.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'Метод ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d9035f6c791708dc0b7d84ffd69380f801f4ecce8525c03bb1ac00a3902a1d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727794"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a>Метод ID3DXSkinInfo:: Финдбоневертексинфлуенцеиндекс

Извлекает индекс кости, влияющей на одну вершину.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*боненум* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс кости. Значение должно находиться в диапазоне от 0 до количества костей.

</dd> <dt>

*вертекснум* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Индекс вершины, для которого влияет влияние на кость. Значение должно находиться в диапазоне от 0 до количества вершин в сетке.

</dd> <dt>

*пинфлуенцеиндекс* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на индекс влияния на кость, влияющих на Вертекснум.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если указанная кость не влияет на данную вершину, \_ возвращается значение false. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Жетбоневертексинфлуенце**](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетбоневертексинфлуенце**](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[**ID3DXSkinInfo:: Жетбонеинфлуенце**](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
