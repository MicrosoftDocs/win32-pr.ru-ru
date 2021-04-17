---
description: Доступ к буферу соседей в сетке.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'Метод ID3DX10Mesh:: Жетаджаценцибуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703897"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a>Метод ID3DX10Mesh:: Жетаджаценцибуффер

Доступ к буферу соседей в сетке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппаджаценци* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Буфер соседства. См. [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




