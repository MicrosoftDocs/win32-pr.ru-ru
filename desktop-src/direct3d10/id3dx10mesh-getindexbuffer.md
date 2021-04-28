---
description: 'Метод ID3DX10Mesh:: Жетиндексбуффер — получает данные в буфере индекса.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'Метод ID3DX10Mesh:: Жетиндексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084032"
---
# <a name="id3dx10meshgetindexbuffer-method"></a>Метод ID3DX10Mesh:: Жетиндексбуффер

Получает данные в буфере индекса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппиндексбуффер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Адрес указателя на интерфейс ID3DX10MeshBuffer, представляющий буфер индекса, связанный с сеткой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




