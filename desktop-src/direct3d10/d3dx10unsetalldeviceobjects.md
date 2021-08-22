---
description: Удаляет все ресурсы с устройства, присвоив их указателям значение NULL. Этот метод должен вызываться во время завершения работы приложения. Это гарантирует, что когда один из них освобождает все ресурсы, которые не привязаны к устройству.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Функция D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 079c5f1b437c2755bf7125dee6be10baed1a91b4a37276997e70543c72904036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128346"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>Функция D3DX10UnsetAllDeviceObjects

Удаляет все ресурсы с устройства, присвоив их указателям **значение NULL**. Этот метод должен вызываться во время завершения работы приложения. Это гарантирует, что когда один из них освобождает все ресурсы, которые не привязаны к устройству.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на устройство. См. раздел [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




