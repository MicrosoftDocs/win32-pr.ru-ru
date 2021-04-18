---
description: Доступ к буферу атрибутов сетки.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'Метод ID3DX10Mesh:: Жетаттрибутебуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703896"
---
# <a name="id3dx10meshgetattributebuffer-method"></a>Метод ID3DX10Mesh:: Жетаттрибутебуффер

Доступ к буферу атрибутов сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппаттрибутебуффер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Буфер атрибута. См. [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

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

 

 




