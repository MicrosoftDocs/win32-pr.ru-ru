---
description: Получение суммы влияния на заданную кость на заданную вершину.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'Метод ID3DX10SkinInfo:: Жетбонеинфлуенце (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b53f642b6e62bb37c6979602b1ae66e09ffc2eb42a6d47c70c6b895a01ba273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096554"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>Метод ID3DX10SkinInfo:: Жетбонеинфлуенце

Получение суммы влияния на заданную кость на заданную вершину.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
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

*пвеигхт* \[ окне\]
</dt> <dd>

Тип: **float \***

Величина влияния (от 0 до 1), на которую кость поверх вершины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть равно E \_ INVALIDARG.

## <a name="remarks"></a>Remarks

Используйте ID3DX10SkinInfo:: Жетбонеинфлуенцекаунт, чтобы узнать, сколько вершин влияет на кость.

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

 

 
