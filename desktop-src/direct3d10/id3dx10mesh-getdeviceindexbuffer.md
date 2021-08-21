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
ms.openlocfilehash: 869bd40b49801a1469ca08baa3a493cc23e6f6238624380411c8d91de829c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990374"
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

## <a name="remarks"></a>Remarks

Если буфер индексов сетки еще не зафиксирован на устройстве, этот API будет автоматически зафиксировать буфер, прежде чем он вернет указатель на буфер.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




