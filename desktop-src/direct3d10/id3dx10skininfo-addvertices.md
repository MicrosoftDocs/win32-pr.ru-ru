---
description: Выделение пространства для дополнительных вершин.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'Метод ID3DX10SkinInfo:: Аддвертицес (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651557"
---
# <a name="id3dx10skininfoaddvertices-method"></a>Метод ID3DX10SkinInfo:: Аддвертицес

Выделение пространства для дополнительных вершин.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число добавляемых вершин.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если этот метод завершился успешно, возвращается значение S \_ ОК. Если метод завершается со сбоем, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.

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

 

 
