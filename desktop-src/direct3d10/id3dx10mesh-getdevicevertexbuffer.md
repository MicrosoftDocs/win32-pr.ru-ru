---
description: 'Доступ к буферу вершин сетки после его фиксации на устройстве с помощью ID3DX10Mesh:: Коммиттодевице. Это отличается от ID3DX10Mesh:: Жетвертексбуффер, который возвращает буфер вершин до того, как он зафиксируется на устройстве.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'Метод ID3DX10Mesh:: Жетдевицевертексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11493392f710fe3fd3bebab5187b61522434b268bf099489d84ea1cc3ec99309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540267"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>Метод ID3DX10Mesh:: Жетдевицевертексбуффер

Доступ к буферу вершин сетки после его фиксации на устройстве с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md). Это отличается от [**ID3DX10Mesh:: жетвертексбуффер**](id3dx10mesh-getvertexbuffer.md), который возвращает буфер вершин до того, как он зафиксируется на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*iBuffer* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс, указывающий, к какому буферу вершин требуется доступ.

</dd> <dt>

*ппвертексбуффер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Буфер вершин после его фиксации на устройстве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requirements (Требования)



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

 

 
