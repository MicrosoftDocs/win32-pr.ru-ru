---
title: Класс CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания подобъекта состояния конфигурации конвейера райтраЦинг с флагами.
keywords:
- Класс CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: fc2049f6a800891e165f57099ad7f9b0bbaba263
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812183"
---
# <a name="cd3dx12_raytracing_pipeline_config1_subobject-class"></a>Класс CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT

Вспомогательный класс для создания подобъекта состояния конфигурации конвейера райтраЦинг с флагами.

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT
{
public:
    CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxTraceRecursionDepth, D3D12_RAYTRACING_PIPELINE_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_PIPELINE_CONFIG1& () const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`Config(UINT, D3D12_RAYTRACING_PIPELINE_FLAGS)`

Функция для настройки ограничения на рекурсию лучей для конвейера райтраЦинг. Также принимает параметр [D3D12_RAYTRACING_PIPELINE_FLAGS](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_flags) .

`Type`

Возвращает тип подобъекта, представленного [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) константой.

`operator const D3D12_STATE_SUBOBJECT&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) объект, описывающий объект состояния.

`operator const D3D12_RAYTRACING_PIPELINE_CONFIG&`

Оператор преобразования, возвращающий ссылку на константу [D3D12_RAYTRACING_PIPELINE_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config) объект, описывающий объект состояния.

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>См. также

* [Вспомогательные структуры для Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
