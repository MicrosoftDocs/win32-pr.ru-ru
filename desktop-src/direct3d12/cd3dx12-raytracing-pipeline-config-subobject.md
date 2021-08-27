---
title: Класс CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT (D3dx12. h)
description: Вспомогательный класс для создания подобъекта состояния конфигурации конвейера райтраЦинг.
keywords:
- Класс CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: bd453455f6090d814e3e53dfb6d9ac32f25a6fb7
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812205"
---
# <a name="cd3dx12_raytracing_pipeline_config_subobject-class"></a>Класс CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT

Вспомогательный класс для создания подобъекта состояния конфигурации конвейера райтраЦинг. См. также [CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT](cd3dx12-raytracing-pipeline-config1-subobject.md).

Дополнительные сведения о вспомогательных параметрах создания объектов состояния D3DX12 см. в разделе [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Синтаксис

```cpp
class CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT
{
    CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxTraceRecursionDepth) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_PIPELINE_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Члены

`CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT`

Конструктор по умолчанию. Создает новый экземпляр **CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT**, инициализированный по умолчанию.

`CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Конструктор, создающий новый экземпляр **CD3DX12_RAYTRACING_PIPELINE_CONFIG_SUBOBJECT** , инициализируемый с помощью содержимого объекта [**CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) .

`Config(UINT)`

Функция для настройки ограничения на рекурсию лучей для конвейера райтраЦинг.

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
* [CD3DX12_RAYTRACING_PIPELINE_CONFIG1_SUBOBJECT](cd3dx12-raytracing-pipeline-config1-subobject.md)
