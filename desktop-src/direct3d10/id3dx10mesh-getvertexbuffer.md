---
description: 'Метод ID3DX10Mesh:: Жетвертексбуффер — получает буфер вершин, связанный с сеткой.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'Метод ID3DX10Mesh:: Жетвертексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108082"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>Метод ID3DX10Mesh:: Жетвертексбуффер

Извлекает буфер вершин, связанный с сеткой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*iBuffer* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Буфер вершин для получения. Это значение индекса.

</dd> <dt>

*ппвертексбуффер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Буфер вершин. См. [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)

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

 

 
