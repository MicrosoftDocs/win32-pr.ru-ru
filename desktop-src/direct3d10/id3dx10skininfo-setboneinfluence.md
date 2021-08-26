---
description: Установка объема влияния на заданную кость на заданную вершину.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'Метод ID3DX10SkinInfo:: Сетбонеинфлуенце (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1bf2f2a6ec92a1e4551bdc22d43bd143c9da5c8114c44619c073a838de52c606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069964"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a>Метод ID3DX10SkinInfo:: Сетбонеинфлуенце

Установка объема влияния на заданную кость на заданную вершину.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Бонеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс, указывающий существующую кость. Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Инфлуенцеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс в списке вершин, на которые она влияет.

</dd> <dt>

*Вес* \[ окне\]
</dt> <dd>

Тип: **float**

Величина влияния (от 0 до 1), на которую кость поверх вершины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть равно E \_ INVALIDARG.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
