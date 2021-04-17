---
title: 'Метод ID3D12DeviceDownlevel:: Куеривидеомеморинфо'
description: 'Копирует содержимое из ресурса Texture2D Direct3D 12 в окно. | Метод ID3D12DeviceDownlevel:: Куеривидеомеморинфо'
keywords:
- Метод Куеривидеомеморинфо
- Метод Куеривидеомеморинфо, интерфейс ID3D12DeviceDownlevel
- Интерфейс ID3D12DeviceDownlevel, метод Куеривидеомеморинфо
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720921"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>Метод ID3D12DeviceDownlevel:: Куеривидеомеморинфо

Предоставляет статистику памяти в Windows 7. Этот метод эквивалентен [IDXGIAdapter3:: куеривидеомеморинфо](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), который недоступен в Windows 7.

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>Параметры

`NodeIndex`

Тип: **uint**

Указывает физический адаптер устройства, для которого запрашиваются данные видеопамяти. Для операции с одним GPU установите значение 0. Если имеется несколько узлов GPU, задайте для него индекс узла (физического адаптера устройства), для которого запрашиваются данные видеопамяти. См. раздел [многоадаптеровые системы](multi-engine.md).

`MemorySegmentGroup`

Тип: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

Указывает **DXGI_MEMORY_SEGMENT_GROUP** , определяющий группу как локальную или нелокальную.

`pVideoMemoryInfo`

Тип: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

Заполняет структуру **DXGI_QUERY_VIDEO_MEMORY_INFO** текущими значениями.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **S_OK** при успешном выполнении или в случае сбоя HRESULT.

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------|------------------|
| Header | d3d12downlevel. h и dxgi1_4. h |
| DLL    | D3D12.dll (только Windows 7) |

## <a name="see-also"></a>См. также раздел
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Интерфейсы Direct3D 12 в Windows 7](direct3d-12on7-interfaces.md)
* [Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
