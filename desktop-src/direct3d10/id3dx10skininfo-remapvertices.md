---
description: Изменение вершин, на которые влияют эти кости.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'Метод ID3DX10SkinInfo:: Ремапвертицес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713705"
---
# <a name="id3dx10skininforemapvertices-method"></a>Метод ID3DX10SkinInfo:: Ремапвертицес

Изменение вершин, на которые влияют эти кости.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Неввертекскаунт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Новое число вершин.

</dd> <dt>

*пвертексремап* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на массив индексов вершин, описывающих повторное сопоставление. Например, пусть Скининфо содержит несколько вершин, таких, что bone0 сопоставляется с v0, bone1 — v1 и bone2 — v2, а массив с 2, 1, 0 — для Пбонеремап. Это приведет к сопоставлению bone0 с v2, bone1 – v1, а bone2 — v0.

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

 

 
