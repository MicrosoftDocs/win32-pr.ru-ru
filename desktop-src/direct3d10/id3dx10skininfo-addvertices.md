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
ms.openlocfilehash: 232778cdec6c8ab1c4874c6dcef3cadb9b1492d12fe1d4d60d787a484a3425c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302470"
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
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
