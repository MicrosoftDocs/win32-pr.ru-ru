---
description: Изменение того, какие кости влияют на вершины.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'Метод ID3DX10SkinInfo:: Ремапбонес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713706"
---
# <a name="id3dx10skininforemapbones-method"></a>Метод ID3DX10SkinInfo:: Ремапбонес

Изменение того, какие кости влияют на вершины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Невбонекаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Новое число костей.

</dd> <dt>

*пбонеремап* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на массив индексов костей, описывающих повторное сопоставление. Например, пусть Скининфо содержит несколько костей, таких, что bone0 сопоставляется с v0, bone1 — v1 и bone2 — v2, а массив с 2, 1, 0 — для Пбонеремап. Это приведет к сопоставлению bone0 с v2, bone1 – v1, а bone2 — v0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY или e \_ INVALIDARG.

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

 

 
