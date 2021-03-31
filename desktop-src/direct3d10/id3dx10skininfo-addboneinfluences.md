---
description: Включите существующую кость, чтобы она влияла на группу вершин, и определите, насколько сильно влияют на эту кость на каждой вершине.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'Метод ID3DX10SkinInfo:: Аддбонеинфлуенцес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273794"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>Метод ID3DX10SkinInfo:: Аддбонеинфлуенцес

Включите существующую кость, чтобы она влияла на группу вершин, и определите, насколько сильно влияют на эту кость на каждой вершине.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Бонеиндекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс, указывающий существующую кость. Значение должно находиться в диапазоне от 0 до значения, возвращаемого [**ID3DX10SkinInfo:: жетнумбонес**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Инфлуенцекаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число вершин, добавляемых к влиянию на кость.

</dd> <dt>

*пиндицес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на массив индексов вершин. Каждый элемент этого массива имеет соответствующий элемент в Пвеигхтс, так что Пиндицес \[ i \] соответствует пвеигхтс \[ i \] . Соответствующее значение в Пвеигхтс \[ i \] определяет, какое влияние на бонеиндекс будет на вершину, индексируемую с помощью пиндицес \[ i \] . Размер массива Пиндицес должен быть больше или равен Инфлуенцекаунт.

</dd> <dt>

*пвеигхтс* \[ окне\]
</dt> <dd>

Тип: **float \***

Указатель на массив весовых коэффициентов костей. Каждый элемент этого массива имеет соответствующий элемент в Пиндицес, так что Пвеигхтс \[ i \] соответствует пиндицес \[ i \] . Каждое значение в Пвеигхтс находится в диапазоне от 0 до 1 и определяет величину влияния на кость на каждую вершину. Размер Пвеигхтс должен быть больше или равен Инфлуенцекаунт.

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

 

 
