---
description: Установите данные вершин в один из буферов вершин сетки.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'Метод ID3DX10Mesh:: Сетвертексдата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59dc5292d5d5dfc269f97f2a8d19ce9a19ea95ceefda47eaf89ac77f81838f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990334"
---
# <a name="id3dx10meshsetvertexdata-method"></a>Метод ID3DX10Mesh:: Сетвертексдата

Установите данные вершин в один из буферов вершин сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*iBuffer* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Буфер вершин, заполняемый с помощью pData.

</dd> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **константа \* void**

Устанавливаемые данные вершин.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
