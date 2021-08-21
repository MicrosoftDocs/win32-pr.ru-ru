---
title: Структура CD3DX12_VIEW_INSTANCING_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) .
keywords:
- Структура CD3DX12_VIEW_INSTANCING_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813253"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>Структура CD3DX12_VIEW_INSTANCING_DESC

Вспомогательная структура, позволяющая легко инициализировать структуру [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Синтаксис

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_VIEW_INSTANCING_DESC`

Конструктор по умолчанию. Создает новый, неинициализированный экземпляр **CD3DX12_VIEW_INSTANCING_DESC**.

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_VIEW_INSTANCING_DESC** , инициализируемый с помощью содержимого структуры [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

Конструктор, создающий новый экземпляр **CD3DX12_VIEW_INSTANCING_DESC** , инициализируемый этими значениями.

|Элемент данных|Значение|
|-|-|
|виевинстанцекаунт|0|
|пвиевинстанцелокатионс|nullptr|
|Флаги|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

Конструктор, создающий новый экземпляр **CD3DX12_VIEW_INSTANCING_DESC** , инициализируемый параметрами, переданными в него.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
