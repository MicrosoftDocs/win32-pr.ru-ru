---
description: 'Удаляет данные сетки с устройства, которое было зафиксировано на устройстве (с помощью ID3DX10Mesh:: Коммиттодевице).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: 'ID3DX10Mesh: метод:D-карты (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674700"
---
# <a name="id3dx10meshdiscard-method"></a>ID3DX10Mesh::D методе кредитной карты

Удаляет данные сетки с устройства, которое было зафиксировано на устройстве (с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md)).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двдискард* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ \_ Флаги удаления сетки D3DX10**](d3dx10-mesh-discard-flags.md)**

Указывает, какие части данных сетки следует отбросить от устройства. См. раздел [**\_ \_ \_ Флаги отказа в сетке D3DX10**](d3dx10-mesh-discard-flags.md).

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

 

 




