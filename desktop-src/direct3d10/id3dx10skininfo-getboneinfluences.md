---
description: Получение списка вершин, на которые влияет заданная кость, и списка интенсивности влияния этой кости на каждую вершину.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'Метод ID3DX10SkinInfo:: Жетбонеинфлуенцес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273972"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>Метод ID3DX10SkinInfo:: Жетбонеинфлуенцес

Получение списка вершин, на которые влияет заданная кость, и списка интенсивности влияния этой кости на каждую вершину.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Бонеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс, указывающий существующую кость. Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Смещение* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Смещение от верхнего края списка влияющих вершин. Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетбонеинфлуенцекаунт**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число индексов и весов, которые необходимо получить. Значение должно находиться в диапазоне от 0 до значения, возвращаемого ID3DX10SkinInfo:: Жетбонеинфлуенцекаунт.

</dd> <dt>

*пдестиндицес* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Список индексов в буфере вершин, каждый из которых представляет вершину, на которую влияет кость. Эти значения соответствуют значениям в Пдествеигхтс, таким, что Пдестиндицес \[ i \] соответствует пдествеигхтс \[ i \] .

</dd> <dt>

*пдествеигхтс* \[ в, out\]
</dt> <dd>

Тип: **float \***

Список величин влияния на кость на каждую вершину. Эти значения соответствуют значениям в Пдестиндицес, таким, что Пдествеигхтс \[ i \] соответствует пдестиндицес \[ i \] . f

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ INVALIDARG или e \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
