---
title: Глобальные уникальные идентификаторы атрибутов адаптера DXCore
description: 'Следующие идентификаторы GUID атрибутов адаптера объявляются в `dxcore_interface.h` и используются с методами [идкскореадаптерфактори:: Креатеадаптерлист](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) и [идкскореадаптер:: исаттрибутесуппортед](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .'
keywords:
- Дкскоре, атрибут адаптера, идентификаторы GUID
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 44b6be239286e13cecbf6eb501b333cba5541f6de1dfd8e217166d9620bdfbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279664"
---
# <a name="dxcore-adapter-attribute-guids"></a>Глобальные уникальные идентификаторы атрибутов адаптера DXCore

Следующие идентификаторы GUID атрибутов адаптера объявляются в `dxcore_interface.h` и используются с методами [идкскореадаптерфактори:: Креатеадаптерлист](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) и [идкскореадаптер:: исаттрибутесуппортед](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) . Для любого заданного адаптера может применяться один или несколько атрибутов.

| GUID | Значение |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Указывает адаптер, который поддерживает использование с графическими API-интерфейсами [Direct3D 11](/windows/win32/direct3d11) . Нет никаких гарантий относительно конкретных функций, и не гарантируется, что ОС в ее текущей конфигурации поддерживает эти API. | 0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Указывает адаптер, который поддерживает использование с графическими API-интерфейсами [Direct3D 12](/windows/win32/direct3d12) . Нет никаких гарантий относительно конкретных функций, и не гарантируется, что ОС в ее текущей конфигурации поддерживает эти API. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8C, 0x96, 0xe8, 0x9e, 0x33, 0x1B, 0x47, 0xB1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Указывает адаптер, который поддерживает использование с API-интерфейсами вычислений [Direct3D 12 Core](../direct3d12/core-feature-levels.md) . Нет никаких гарантий относительно конкретных функций, и не гарантируется, что ОС в ее текущей конфигурации поддерживает эти API. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xAA, 0x23, 0xa6, 0xde, 0x1B, 0xE0, 0x90 |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Заголовок | dxcore_interface. h |

## <a name="see-also"></a>См. также раздел

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Справочник по Дкскоре](./dxcore-reference.md)
* [Перечисление адаптеров с использованием DXCore](./dxcore-enum-adapters.md)
* [Графика Direct3D 12](../direct3d12/direct3d-12-graphics.md)
