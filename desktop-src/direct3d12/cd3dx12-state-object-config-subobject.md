---
title: Класс CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания подобъекта, определяющего общие свойства объекта State.
keywords:
- Класс CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 294dda04f9550e437f91f6f5595206a4113a975ee182ac900b6c4804b3100fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346568"
---
# <a name="cd3dx12_state_object_config_subobject-class"></a>Класс CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT

Вспомогательный класс для создания подобъекта, определяющего общие свойства объекта State.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
{
public:
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetFlags(D3D12_STATE_OBJECT_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_STATE_OBJECT_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetFlags(D3D12_STATE_OBJECT_FLAGS)`

Функция для указания требований для объекта состояния через объект [D3D12_STATE_OBJECT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_flags) .

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator const D3D12_STATE_OBJECT_CONFIG&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) объект, описывающий объект состояния.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также раздел

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
