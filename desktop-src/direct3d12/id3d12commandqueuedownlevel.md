---
title: Интерфейс ID3D12CommandQueueDownlevel
description: Предоставляет механизм присутствия, характерный для Windows 7.
keywords:
- Интерфейс ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720868"
---
# <a name="id3d12commandqueuedownlevel-interface"></a>Интерфейс ID3D12CommandQueueDownlevel

Доступ к этому интерфейсу можно получить через **QueryInterface** из [очереди команд Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) при использовании [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Он предоставляет механизм присутствия, характерный для Windows 7.

### <a name="methods"></a>Методы

Интерфейс **ID3D12CommandQueueDownlevel** содержит следующие методы.

| Метод | Описание |
|:-------|:------------|
| [**Настоящее**](id3d12commandqueuedownlevel-present.md) | Копирует содержимое из ресурса D3D12 Texture2D в окно. |

## <a name="requirements"></a>Требования

| Требование | Значение |
|--------|------------------|
| Header | d3d12downlevel. h |
| DLL    | D3D12.dll (только Windows 7) |

## <a name="see-also"></a>См. также раздел
* [Интерфейсы Direct3D 12 в Windows 7](direct3d-12on7-interfaces.md)
* [Справочник по Direct3D 12 в Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
