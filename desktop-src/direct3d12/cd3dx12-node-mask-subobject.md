---
title: Класс CD3DX12_NODE_MASK_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания подобъекта State, определяющего узлы GPU, к которым применяется объект состояния.
keywords:
- Класс CD3DX12_NODE_MASK_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_NODE_MASK_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: bfa1c5ce1facb946b060bf7501c09c6c13cfca13
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812903"
---
# <a name="cd3dx12_node_mask_subobject-class"></a>Класс CD3DX12_NODE_MASK_SUBOBJECT

Вспомогательный класс для создания подобъекта State, определяющего узлы GPU, к которым применяется объект состояния.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_NODE_MASK_SUBOBJECT
{
    CD3DX12_NODE_MASK_SUBOBJECT() noexcept;
    CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetNodeMask(UINT NodeMask) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_NODE_MASK& () const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_NODE_MASK_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_NODE_MASK_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_NODE_MASK_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`SetNodeMask(UINT)`

Функция для установки маски узла.

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_NODE_MASK](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator const D3D12_NODE_MASK&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_NODE_MASK](/windows/win32/api/d3d12/ns-d3d12-d3d12_node_mask) объект, описывающий объект состояния.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
