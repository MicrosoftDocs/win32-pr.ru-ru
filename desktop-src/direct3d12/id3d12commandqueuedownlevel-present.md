---
title: 'ID3D12CommandQueueDownlevel: метод повторной отправки:P'
description: 'Копирует содержимое из ресурса Texture2D Direct3D 12 в окно. | ID3D12CommandQueueDownlevel: метод повторной отправки:P'
keywords:
- Метод Present
- Метод Present, интерфейс ID3D12CommandQueueDownlevel
- Интерфейс ID3D12CommandQueueDownlevel, метод Present
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720922"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel: метод повторной отправки:P

Копирует содержимое из ресурса Texture2D Direct3D 12 в окно.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>Параметры

`pOpenCommandList`

Тип: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Список открытых команд, который Direct3D 12 помещает в очередь на текущую команду, а затем закрывается и отправляется.

`pSourceTex2D`

Тип: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Ресурс, содержащий необходимое содержимое для показа, с измерением [**ресурса измерения D3D12 \_ \_ \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)и форматом, который является одним из следующих.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Тип: **[HWND](/windows/desktop/WinProg/windows-data-types)**

Маркер окна, в котором должно отображаться содержимое.

`Flags`

Тип: **[ \_ \_ \_ Флаги представления нижнего уровня D3D12](d3d12_downlevel_present_flags.md)**

Флаги для изменения **текущей** операции.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **S_OK** при успешном выполнении или в случае сбоя HRESULT.

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------|------------------|
| Header | d3d12downlevel. h |
| DLL    | D3D12.dll (только Windows 7) |

## <a name="see-also"></a>См. также раздел
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Интерфейсы Direct3D 12 в Windows 7](direct3d-12on7-interfaces.md)
* [Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
