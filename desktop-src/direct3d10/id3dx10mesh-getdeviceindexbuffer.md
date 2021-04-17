---
description: 'Доступ к буферу индекса сетки после его фиксации на устройстве с помощью ID3DX10Mesh:: Коммиттодевице. Это отличается от ID3DX10Mesh:: Жетиндексбуффер, который возвращает буфер индекса до того, как он зафиксируется на устройстве.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'Метод ID3DX10Mesh:: Жетдевицеиндексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694234"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>Метод ID3DX10Mesh:: Жетдевицеиндексбуффер

Доступ к буферу индекса сетки после его фиксации на устройстве с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md). Это отличается от [**ID3DX10Mesh:: жетиндексбуффер**](id3dx10mesh-getindexbuffer.md), который возвращает буфер индекса до того, как он зафиксируется на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппиндексбуффер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Буфер индекса после его фиксации на устройстве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Комментарии

Если буфер индексов сетки еще не зафиксирован на устройстве, этот API будет автоматически зафиксировать буфер, прежде чем он вернет указатель на буфер.

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

 

 




